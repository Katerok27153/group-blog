---
title: Этап 4. Модель колебаний цепочек. Полный цикл исследования

event: Групповой проект. Этап 4
event_url: 

location: РУДН
address:
  street: 
  city: Москва
  region:
  postcode:
  country: Россия

summary: Выполнено полное исследование колебаний одномерных цепочек в гармоническом и ангармоническом приближениях. Разработаны алгоритм и комплекс программ на Julia, подтверждено дисперсионное соотношение, независимость мод в линейном случае и воспроизведён классический эффект возврата Ферми‑Паста‑Улама.
abstract: 'На четвёртом этапе группового проекта представлен законченный цикл работы над моделью колебаний цепочек. Выполнено теоретическое описание гармонического и ангармонического приближений, выведены уравнения движения и дисперсионное соотношение. Разработан детальный алгоритм из 7 шагов - задание параметров, дискретизация, инициализация, численное интегрирование (схема «чехарда» и метод Верле), анализ распределения энергии по модам через дискретное синус‑преобразование (DST), исследование ангармонических эффектов и визуализация. Реализован комплекс из 5 программ на Julia - моделирование гармонической цепочки, измерение собственных частот (отклонение для чётных мод <1%), проверка независимости мод, расчёт цепочки с чередующимися массами (mlight=1, mheavy=2) и воспроизведение FPU‑возврата при α=0.5. Результаты подтверждают теоретические предсказания и качественно воспроизводят классические результаты Ферми, Пасты и Улама.'

# Talk start and end times.
#   End time can optionally be hidden by prefixing the line with `#`.
date: '2026-05-14T13:00:00Z'
date_end: '2026-05-14T15:00:00Z'
all_day: false

# Schedule page publish date (NOT talk date).
publishDate: '2026-01-01T00:00:00Z'

authors: [mobyzova, eavernikovskaya, oskalashnikova, aabogatkina, ansusenko]
tags: ["численное моделирование", "Ферми-Паста-Улам", "Julia", "гармоническая цепочка", "ангармоническая цепочка", "нормальные моды", "дискретное синус-преобразование", "FPU-возврат", "сверхпериодичность"]

# Is this a featured talk? (true/false)
featured: false

image:
  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/bzdhc5b3Bxs)'
  focal_point: Right

url_code: ''
url_pdf: 'https://drive.google.com/file/d/1XzgMwxDU-LAiTo6uTA_HMhWwAb9SVpn9/view?usp=sharing'
url_slides: 'https://drive.google.com/file/d/1AXHwDf_1_h53pxBJItsMAOWTpnSIoNr0/view?usp=sharing'

# Custom links для двух видео
links:
  - name: Коды
    url: 'https://drive.google.com/file/d/1N0UL_G728xvqp_COpMaiwtimliTKzwLW/view?usp=sharing'
  - name: Rutube
    url: 'https://rutube.ru/video/private/6053c67de508e22357b7b422f49a8d93/?p=XCJKKi3tzdHNe1Zw-hfELQ'
    icon_pack: fab
    icon: rutube
  - name: VK Видео
    url: 'https://vkvideo.ru/video-232514568_456239230?pl=-232514568_51'
    icon_pack: fab
    icon: vk
  - name: GitHub
    url: 'https://github.com/Katerok27153/study_2025-2026_mathmod.git'
    icon_pack: fab
    icon: github
  - name: Релиз на GitHub
    url: 'https://github.com/Katerok27153/study_2025-2026_mathmod/releases/tag/v4.0.1'
    icon_pack: fas
    icon: download
  - name: GitVerse
    url: 'https://gitverse.ru/Katerok27153/study_2025-2026_mathmod.git'
    icon_pack: fab
    icon: git
  - name: Релиз на GitVerse
    url: 'https://gitverse.ru/Katerok27153/study_2025-2026_mathmod/releases/tag/v4.0.1'
    icon_pack: fas
    icon: download

# Markdown Slides (optional).
#   Associate this talk with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides:

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects:
---

## О проекте

### Что делали
На четвёртом этапе представлен **законченный цикл исследования** колебаний одномерных цепочек: от вывода уравнений до численного моделирования и анализа. Работа разделена на три крупные части.

### Теоретическое описание задачи
- Выведены уравнения движения для гармонической цепочки с неподвижными концами $m \frac{d^2 y_i}{dt^2} = k(y_{i+1} - 2y_i + y_{i-1})$
- Получено дисперсионное соотношение для нормальных мод $\omega_l = 2\omega_0 \sin\left(\frac{l\pi}{2(N+1)}\right),\quad \omega_0=\sqrt{\frac{k}{m}}$
- Описано ангармоническое приближение (задача Ферми‑Паста‑Улама) с кубической поправкой и нелинейным уравнением движения $m \frac{d^2 y_i}{dt^2} = k\left[(y_{i+1}-2y_i+y_{i-1}) - \frac{3\alpha}{2d}\left((y_{i+1}-y_i)^2-(y_i-y_{i-1})^2\right)\right]$

### Детальный алгоритм
1. **Задание параметров** — $m$, $k$, $d$, $N$, $\alpha$, начальные смещения/скорости, тип возбуждения.
2. **Дискретизация** — выбор $\Delta t$ с учётом условия Куранта, определение $T_{\text{max}}$.
3. **Инициализация** — равновесные координаты $x_i^0 = i \cdot d$, начальные смещения по форме моды.
4. **Численное интегрирование** — схема «чехарда» (leapfrog) для гармонического случая и метод Velocity Verlet для ангармонического.
5. **Анализ энергии по модам** — дискретное синус‑преобразование (DST):

$$
b_l(t) = \frac{2}{N}\sum_{j=1}^{N} y_j(t) \sin\left(\frac{\pi l j}{N+1}\right), \quad
E_l(t) = \frac12 \left(\dot b_l^2 + \omega_l^2 b_l^2\right)
$$

6. **Исследование ангармонических эффектов** — наблюдение квазипериодичности, FPU‑возврата и сверхпериодичности.
7. **Визуализация** — графики смещений, спектрограммы энергии мод, анимации.

### Программная реализация (5 скриптов на Julia)
| Скрипт | Задача | Ключевые результаты |
|--------|--------|----------------------|
| `task1.jl` | Моделирование гармонической цепочки ($N=32$, $m=1$, $k=1$, $\Delta t=0.01$) | Устойчивое интегрирование, подтверждение корректности схемы |
| `task2.jl` | Измерение собственных частот мод $l=1\dots 5$ | Отличное совпадение для чётных мод (<1% отклонения); нечётные моды дают погрешность до 32% из‑за метода пересечения нуля |
| `task3.jl` | Проверка независимости мод | Энергия первой моды остаётся $\approx 1$, остальные моды $\approx 0$ — моды независимы |
| `task4.jl` | Цепочка с чередующимися массами ($m_{\text{light}}=1$, $m_{\text{heavy}}=2$) | Моделирование бинарной структуры типа NaCl, индивидуальное ускорение для каждой частицы |
| `task5.jl` | Ангармоническая цепочка. Задача Ферми‑Паста‑Улама ($\alpha=0.5$, $A=0.2$) | **Качественное воспроизведение FPU‑возврата** — энергия концентрируется в низших модах и циклически возвращается в первую моду, вопреки ожидаемой термализации |

### Основные научные результаты
- **Подтверждено дисперсионное соотношение** для гармонической цепочки (экспериментальные частоты для чётных мод совпадают с теорией с точностью <1%).
- **Верифицирована независимость нормальных мод** в линейном приближении — энергия не перетекает между модами.
- **Промоделирована цепочка с бинарным составом** (чередование масс 1 и 2), что имитирует реальные ионные кристаллы.
- **Воспроизведён классический эффект Ферми‑Паста‑Улама**: в ангармонической цепочке с $\alpha=0.5$ и возбуждением первой моды наблюдается рекурренция энергии, а не термализация. Это один из первых численных экспериментов, положивших начало нелинейной динамике.

### Параметры всех моделей
| Параметр | Значение |
|----------|----------|
| Число частиц $N$ | 32 |
| Масса (гармоническая) | 1 |
| Массы (чередующиеся) | 1 (нечётные) / 2 (чётные) |
| Жёсткость пружин $k$ | 1 |
| Равновесное расстояние $d$ | 1 |
| Коэф. ангармонизма $\alpha$ | 0.5 (только FPU) |
| $\Delta t$ (task1,3,5) | 0.01 |
| $\Delta t$ (task2,4) | 0.001 |
| $T_{\text{max}}$ | от 100 до 5000 |


## Материалы проекта

- **[Скачать отчёт (PDF)](https://drive.google.com/file/d/1XzgMwxDU-LAiTo6uTA_HMhWwAb9SVpn9/view?usp=sharing)** — полное теоретическое описание
- **[Скачать презентацию (PDF)](https://drive.google.com/file/d/1AXHwDf_1_h53pxBJItsMAOWTpnSIoNr0/view?usp=sharing)** — слайды защиты
- **[Смотреть на Rutube](https://rutube.ru/video/private/6053c67de508e22357b7b422f49a8d93/?p=XCJKKi3tzdHNe1Zw-hfELQ)** — видео защиты
- **[Плейлист на Rutube](https://rutube.ru/plst/1633490)** — плейлист
- **[Смотреть в VK Видео](https://vkvideo.ru/video-232514568_456239230?pl=-232514568_51)** — видео защиты
- **[Плейлист в VK Видео](https://vkvideo.ru/playlist/-232514568_51)** — плейлист
- **[Репозиторий на GitHub](https://github.com/Katerok27153/study_2025-2026_mathmod.git)** — репозиторий проекта
- **[Релиз на GitHub](https://github.com/Katerok27153/study_2025-2026_mathmod/releases/tag/v4.0.1)** — релиз проекта
- **[Репозиторий на GitVerse](https://gitverse.ru/Katerok27153/study_2025-2026_mathmod.git)** — репозиторий проекта
- **[Релиз на GitVerse](https://gitverse.ru/Katerok27153/study_2025-2026_mathmod/releases/tag/v4.0.1)** — релиз проекта
- **[Архив с кодами (ZIP)](https://drive.google.com/file/d/1N0UL_G728xvqp_COpMaiwtimliTKzwLW/view?usp=sharing)** - task1.jl - task5.jl
