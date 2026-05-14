---
title: 'Этап 4. Модель колебаний цепочек. Полный цикл исследования. Публикация'

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors: [mobyzova, eavernikovskaya, oskalashnikova, aabogatkina, ansusenko]

# Author notes (optional)
author_notes:
  - 'Equal contribution'
  - 'Equal contribution'
  - 'Equal contribution'
  - 'Equal contribution'
  - 'Equal contribution'

date: '2026-04-30T00:00:00Z'
doi: ''

# Schedule page publish date (NOT publication's date).
publishDate: '2026-05-14T00:00:00Z'

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ['paper-conference']

# Publication name and optional abbreviated publication name.
publication: In *Групповой проект. Математическое моделирование, РУДН*
publication_short: In *ГП РУДН*

abstract: На четвёртом этапе группового проекта представлен законченный цикл исследования колебаний одномерных цепочек. Выполнено теоретическое описание гармонического и ангармонического приближений, выведены уравнения движения и дисперсионное соотношение. Разработан детальный 7-шаговый алгоритм численного моделирования. Реализован комплекс из 5 программ на Julia - моделирование гармонической цепочки со схемой «чехарда», измерение собственных частот нормальных мод с проверкой дисперсионного соотношения, анализ независимости мод через дискретное синус-преобразование (DST), моделирование цепочки с чередующимися массами (типа NaCl) и исследование ангармонической задачи Ферми-Паста-Улама (FPU) с наблюдением эффекта рекурренции энергии. Все программы протестированы и готовы к использованию.

# Summary. An optional shortened abstract.
summary: Полный цикл исследования колебаний одномерных цепочек. Теория, 7-шаговый алгоритм, 5 программ на Julia. Гармоническая цепочка, измерение частот (отклонение <1% для чётных мод), независимость мод, чередующиеся массы, задача Ферми-Паста-Улама (FPU-возврат).

tags: ["Численное моделирование", "Ферми-Паста-Улам", "Julia", "Гармоническая цепочка", "Ангармоническая цепочка", "Нормальные моды", "Дискретное синус-преобразование", "FPU-возврат", "Сверхпериодичность"]

# Display this page in the Featured widget?
featured: true

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_code: ''
url_pdf: 'https://drive.google.com/file/d/1XzgMwxDU-LAiTo6uTA_HMhWwAb9SVpn9/view?usp=sharing'
url_slides: 'https://drive.google.com/file/d/1AXHwDf_1_h53pxBJItsMAOWTpnSIoNr0/view?usp=sharing'

# Custom links для двух видео
links:
  - name: Slides
    url: 'https://drive.google.com/file/d/1AXHwDf_1_h53pxBJItsMAOWTpnSIoNr0/view?usp=sharing'
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

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
image:
  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/pLCdAaMFLTE)'
  focal_point: ''
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects:
  - example

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: example
---

## О проекте

### Что делали
На четвёртом этапе представлен **законченный цикл исследования** колебаний одномерных цепочек: от вывода уравнений до численного моделирования и анализа результатов.

### Три основных блока работы

#### 1. Теоретическое описание задачи

- Выведены уравнения движения для гармонической цепочки с неподвижными концами: $m \frac{d^2 y_i}{dt^2} = k(y_{i+1} - 2y_i + y_{i-1}), \quad i = 1 \dots N$

- Получено дисперсионное соотношение для нормальных мод: $\omega_l = 2\omega_0 \sin\left(\frac{l\pi}{2(N+1)}\right), \quad \omega_0 = \sqrt{\frac{k}{m}}$

- Описано ангармоническое приближение (задача Ферми-Паста-Улама) с кубической поправкой: $m \frac{d^2 y_i}{dt^2} = k\left[(y_{i+1} - 2y_i + y_{i-1}) - \frac{3\alpha}{2d}\left((y_{i+1} - y_i)^2 - (y_i - y_{i-1})^2\right)\right]$

#### 2. Детальный алгоритм (7 шагов)

1. **Задание параметров системы** — $m$, $k$, $d$, $N$, $\alpha$, начальные смещения/скорости, амплитуда $A$, номер моды $l$
2. **Настройка дискретизации** — выбор $\Delta t$ с учётом условия Куранта, определение $T_{\text{max}} = N_t \cdot \Delta t$
3. **Инициализация системы** — равновесные координаты $x_i^0 = i \cdot d$, начальные смещения $y_i(0) = A \sin(\pi l i/(N+1))$
4. **Численное интегрирование** — схема «чехарда» (leapfrog) для гармонического случая, метод Velocity Verlet для ангармонического
5. **Анализ энергии по модам** — дискретное синус-преобразование (DST) и вычисление $E_l(t)$
6. **Исследование ангармонических эффектов** — наблюдение квазипериодичности, FPU-возврата и сверхпериодичности
7. **Визуализация результатов** — графики смещений и распределения энергии по модам

#### 3. Программная реализация (5 скриптов на Julia)

| Скрипт | Задача | Ключевые результаты |
|--------|--------|----------------------|
| `task1.jl` | Гармоническая цепочка (схема «чехарда») | Устойчивое интегрирование, N=32, m=1, k=1, Δt=0.01, T=100 |
| `task2.jl` | Измерение собственных частот (l=1..5) | Чётные моды: отклонение <1%; нечётные: до 32% (метод пересечения нуля) |
| `task3.jl` | Анализ независимости мод (DST) | Энергия 1-й моды ≈1, остальные ≈0 — моды независимы |
| `task4.jl` | Цепочка с чередующимися массами | $m_{\text{light}}=1$, $m_{\text{heavy}}=2$, бинарная структура (типа NaCl) |
| `task5.jl` | Ангармоническая цепочка. Задача Ферми-Паста-Улама | $\alpha=0.5$, $A=0.2$, **FPU-возврат** — рекурренция энергии мод |

### Основные научные результаты
- **Подтверждено дисперсионное соотношение** — экспериментальные частоты для чётных мод совпадают с теорией с точностью <1%
- **Верифицирована независимость нормальных мод** в линейном приближении — энергия не перетекает между модами
- **Промоделирована цепочка с бинарным составом** (чередование масс 1 и 2), имитирующая ионные кристаллы типа NaCl
- **Воспроизведён классический эффект Ферми-Паста-Улама** — в ангармонической цепочке наблюдается рекурренция энергии, а не термализация

### Технические детали реализации

- **Язык программирования**: Julia 1.9+
- **Ключевые пакеты**: Plots.jl (визуализация)
- **Методы интегрирования**: leapfrog (схема «чехарда»), Velocity Verlet
- **Анализ мод**: дискретное синус-преобразование (DST) с ортонормировкой

### Параметры моделей

| Параметр | Значение |
|----------|----------|
| Число частиц $N$ | 32 |
| Масса (гармоническая) | 1.0 |
| Массы (чередующиеся) | 1.0 (нечётные) / 2.0 (чётные) |
| Жёсткость пружин $k$ | 1.0 |
| Равновесное расстояние $d$ | 1.0 |
| Шаг по времени $\Delta t$ (task1,3,5) | 0.01 |
| Шаг по времени $\Delta t$ (task2,4) | 0.001 |
| Коэффициент ангармонизма $\alpha$ | 0.5 (только task5) |
| Амплитуда $A$ (task5) | 0.2 |

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
