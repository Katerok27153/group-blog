---
title: 'Этап 3. Модель колебаний цепочек. Комплекс программ для решения задачи о колебаниях цепочек. Публикация'

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
publishDate: '2026-04-30T00:00:00Z'

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ['paper-conference']

# Publication name and optional abbreviated publication name.
publication: In *Групповой проект. Математическое моделирование, РУДН*
publication_short: In *ГП РУДН*

abstract: На третьем этапе группового проекта представлена программная реализация моделирования колебаний одномерных цепочек частиц на языке Julia. Разработаны пять программ - моделирование гармонической цепочки со схемой «чехарда», измерение собственных частот нормальных мод с проверкой дисперсионного соотношения, анализ независимости мод через дискретное синус-преобразование (DST), моделирование цепочки с чередующимися массами (типа NaCl) и исследование ангармонической задачи Ферми-Паста-Улама (FPU) с наблюдением эффекта рекурренции энергии. Все программы протестированы и готовы к использованию.

# Summary. An optional shortened abstract.
summary: Комплекс программ на Julia для моделирования колебаний одномерных цепочек. Гармоническая цепочка, измерение частот, анализ независимости мод, чередующиеся массы, задача Ферми-Паста-Улама (FPU-возврат).

tags: ["Численное Моделирование", "Ферми-Паста-Улам", "Julia", "Гармоническая цепочка", "Ангармоническая цепочка", "Нормальные моды", "Дискретное синус-преобразование"]

# Display this page in the Featured widget?
featured: true

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_code: ''
url_pdf: 'https://drive.google.com/file/d/1RmWuQRH_DTpkUBbi06U9XcyT5nokR6ym/view?usp=sharing'
url_slides: 'https://drive.google.com/file/d/1wRPP96B8eEdxANnxC7ucvXSVnOzxa6B1/view?usp=sharing'

# Custom links для двух видео
links:
  - name: Slides
    url: 'https://drive.google.com/file/d/1wRPP96B8eEdxANnxC7ucvXSVnOzxa6B1/view?usp=sharing'
  - name: Коды
    url: 'https://drive.google.com/file/d/1N0UL_G728xvqp_COpMaiwtimliTKzwLW/view?usp=sharing'
  - name: Rutube
    url: 'https://rutube.ru/video/private/405b6010def42895b6274dbc9ed23bcb/?p=sP34Q8XCii8bO1riyRJySg'
    icon_pack: fab
    icon: rutube
  - name: VK Видео
    url: 'https://vkvideo.ru/video-232514568_456239212?pl=-232514568_46'
    icon_pack: fab
    icon: vk
  - name: GitHub
    url: 'https://github.com/Katerok27153/study_2025-2026_mathmod.git'
    icon_pack: fab
    icon: github
  - name: Релиз на GitHub
    url: 'https://github.com/Katerok27153/study_2025-2026_mathmod/releases/tag/v3.0.1'
    icon_pack: fas
    icon: download
  - name: GitVerse
    url: 'https://gitverse.ru/Katerok27153/study_2025-2026_mathmod.git'
    icon_pack: fab
    icon: git
  - name: Релиз на GitVerse
    url: 'https://gitverse.ru/Katerok27153/study_2025-2026_mathmod/releases/tag/v3.0.1'
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
На третьем этапе разработан комплекс программ на языке Julia, реализующий численное моделирование колебаний одномерных цепочек частиц в гармоническом и ангармоническом приближениях.

### Пять реализованных программ

1. **Гармоническая цепочка (task1.jl)**
   - Численное интегрирование схемы «чехарда» (leapfrog)
   - Параметры: N = 32, m = 1, k = 1, Δt = 0.01, T = 100
   - Начальное условие — первая нормальная мода

2. **Измерение собственных частот (task2.jl)**
   - Определение частоты по пересечениям нуля
   - Сравнение с теоретическим дисперсионным соотношением
   - Отклонение для чётных мод < 1%, для нечётных — до 32% (из-за метода измерения)

3. **Анализ независимости нормальных мод (task3.jl)**
   - Дискретное синус-преобразование (DST) с ортонормировкой
   - Вычисление энергии первых пяти мод
   - Подтверждение отсутствия перетекания энергии между модами в гармоническом случае

4. **Цепочка с чередующимися массами (task4.jl)**
   - m_light = 1, m_heavy = 2
   - Моделирование бинарной кристаллической структуры (типа NaCl)
   - Индивидуальное ускорение для каждой частицы

5. **Ангармоническая цепочка. Задача Ферми-Паста-Улама (task5.jl)**
   - Кубическая нелинейность: α = 0.5
   - Метод Velocity Verlet
   - Наблюдение FPU-возврата (рекурренции энергии)

### Основные результаты этапа
- Разработаны 5 рабочих программ на Julia, прошедших тестирование
- Подтверждено дисперсионное соотношение для нормальных мод
- Экспериментально проверена независимость мод в линейном приближении
- Промоделирована цепочка с чередующимися массами
- Качественно воспроизведён классический эффект FPU-возврата

### Технические детали реализации

- **Язык программирования**: Julia 1.9+
- **Ключевые пакеты**: Plots.jl (визуализация), FFTW.jl (быстрое преобразование Фурье)
- **Объём кода**: ~300 строк с документацией
- **Время счёта**: для N=32 частиц, T=10000 шагов ~2 секунды

### Параметры по умолчанию

| Параметр | Значение |
|----------|----------|
| Число частиц N | 32 |
| Масса частицы m | 1.0 |
| Жёсткость пружин k | 1.0 |
| Равновесное расстояние | 1.0 |
| Шаг по времени Δt | 0.05 |
| Число шагов | 10000 |
| Коэффициент ангармонизма β | 0.1, 0.25, 0.5 |

## Материалы проекта

- **[Скачать отчёт (PDF)](https://drive.google.com/file/d/1RmWuQRH_DTpkUBbi06U9XcyT5nokR6ym/view?usp=sharing)** — полное теоретическое описание
- **[Скачать презентацию (PDF)](https://drive.google.com/file/d/1wRPP96B8eEdxANnxC7ucvXSVnOzxa6B1/view?usp=sharing)** — слайды защиты
- **[Смотреть на Rutube](https://rutube.ru/video/private/405b6010def42895b6274dbc9ed23bcb/?p=sP34Q8XCii8bO1riyRJySg)** — видео защиты
- **[Плейлист на Rutube](https://rutube.ru/plst/1613333)** — плейлист
- **[Смотреть в VK Видео](https://vkvideo.ru/video-232514568_456239212?pl=-232514568_46)** — видео защиты
- **[Плейлист в VK Видео](https://vkvideo.ru/playlist/-232514568_46)** — плейлист
- **[Репозиторий на GitHub](https://github.com/Katerok27153/study_2025-2026_mathmod.git)** — репозиторий проекта
- **[Релиз на GitHub](https://github.com/Katerok27153/study_2025-2026_mathmod/releases/tag/v3.0.1)** — релиз проекта
- **[Репозиторий на GitVerse](https://gitverse.ru/Katerok27153/study_2025-2026_mathmod.git)** — репозиторий проекта
- **[Релиз на GitVerse](https://gitverse.ru/Katerok27153/study_2025-2026_mathmod/releases/tag/v3.0.1)** — релиз проекта
- **[Архив с кодами (ZIP)](https://drive.google.com/file/d/1N0UL_G728xvqp_COpMaiwtimliTKzwLW/view?usp=sharing)** - task1.jl - task5.jl
