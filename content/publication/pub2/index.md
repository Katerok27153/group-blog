---
title: 'Этап 2. Модель колебаний цепочек. Алгоритм решения задачи о колебаниях цепочек. Публикация'

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

date: '2026-03-19T00:00:00Z'
doi: ''

# Schedule page publish date (NOT publication's date).
publishDate: '2026-04-09T00:00:00Z'

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ['paper-conference']

# Publication name and optional abbreviated publication name.
publication: In *Групповой проект. Математическое моделирование, РУДН*
publication_short: In *ГП РУДН*

abstract: На втором этапе группового проекта описан алгоритм решения задачи моделирования колебаний одномерных цепочек частиц. Рассмотрены семь ключевых этапов алгоритма - задание параметров системы, настройка дискретизации, инициализация системы, численное интегрирование уравнений движения (схема «чехарда»), анализ распределения энергии по нормальным модам через дискретное синус-преобразование, исследование ангармонических эффектов в задаче Ферми-Паста-Улама (FPU) и визуализация результатов. Особое внимание уделено условиям устойчивости и контролю сохранения энергии. 

# Summary. An optional shortened abstract.
summary: Алгоритм моделирования колебаний одномерной цепочки осцилляторов. Численное интегрирование, анализ мод энергии, задача Ферми-Паста-Улама.

tags: ["Численное Моделирование", "Ферми-Паста-Улам", "Колебания", "Цепочка Осцилляторов", "Алгоритм", "Схема Чехарда"]

# Display this page in the Featured widget?
featured: true

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_code: ''
url_pdf: 'https://drive.google.com/file/d/1MVOcppY5sd-yH-0OkM14oBb1zJ1Y_vMp/view?usp=sharing'
url_slides: 'https://drive.google.com/file/d/1JtF1x5ad_eMQEO_-Jfe2J6rWdUQDsotH/view?usp=sharing'

# Custom links для двух видео
links:
  - name: Slides
    url: 'https://drive.google.com/file/d/1JtF1x5ad_eMQEO_-Jfe2J6rWdUQDsotH/view?usp=sharing'
  - name: Rutube
    url: 'https://rutube.ru/video/private/62f1bf84116345a6ca84c96fe41d5f3b/?p=6-YF43xW9ueeR4JPwTvTGQ'
    icon_pack: fab
    icon: rutube
  - name: VK Видео
    url: 'https://vkvideo.ru/video-232514568_456239193'
    icon_pack: fab
    icon: vk
  - name: GitHub
    url: 'https://github.com/Katerok27153/study_2025-2026_mathmod.git'
    icon_pack: fab
    icon: github
  - name: Релиз на GitHub
    url: 'https://github.com/Katerok27153/study_2025-2026_mathmod/releases/tag/v2.0.1'
    icon_pack: fas
    icon: download
  - name: GitVerse
    url: 'https://gitverse.ru/Katerok27153/study_2025-2026_mathmod.git'
    icon_pack: fab
    icon: git
  - name: Релиз на GitVerse
    url: 'https://gitverse.ru/Katerok27153/study_2025-2026_mathmod/releases/tag/v2.0.1'
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
На втором этапе проекта разработали и описали алгоритм численного решения задачи о колебаниях одномерной цепочки частиц. Алгоритм реализован в виде последовательности шагов, готовых для программной реализации

### Семь шагов алгоритма
1. **Задание параметров системы** — физические параметры (масса, жёсткость, число частиц, коэффициент ангармонизма) и начальные условия (смещения, скорости, тип возбуждения)
2. **Настройка дискретизации** — выбор временного шага Δt с учётом условия устойчивости Куранта-Фридрихса-Леви (CFL)
3. **Инициализация системы** — задание равновесных координат и начальных смещений (например, в виде синусоиды для первой моды)
4. **Численное интегрирование** — явная конечно-разностная схема «чехарда» (leapfrog) с контролем сохранения полной энергии
5. **Анализ распределения энергии по модам** — дискретное синус-преобразование и вычисление энергии каждой нормальной моды
6. **Исследование ангармонических эффектов** — моделирование задачи Ферми-Паста-Улама: наблюдение квазипериодичности, возвратов и сверхпериодичности
7. **Визуализация результатов** — построение графиков смещений частиц, энергий мод во времени и фазовых портретов

### Основные результаты этапа
- Описан полный алгоритм моделирования от задания параметров до визуализации
- Выведены уравнения движения для гармонического и ангармонического случаев
- Приведена схема «чехарда» для интегрирования уравнений второго порядка
- Описан метод перехода в пространство нормальных мод через дискретное синус-преобразование
- Сформулированы критерии устойчивости и контроля точности (сохранение энергии)

### Параметры модели
- Число частиц: 32
- Масса частицы: 1
- Жесткость пружин: 1
- Равновесное расстояние: 1
- Коэффициент ангармонизма: 0.1 / 0.25 / 0.5 (для исследования)

## Материалы проекта

- **[Скачать отчёт (PDF)](https://drive.google.com/file/d/1MVOcppY5sd-yH-0OkM14oBb1zJ1Y_vMp/view?usp=sharing)** — полное теоретическое описание
- **[Скачать презентацию (PDF)](https://drive.google.com/file/d/1JtF1x5ad_eMQEO_-Jfe2J6rWdUQDsotH/view?usp=sharing)** — слайды защиты
- **[Смотреть на Rutube](https://rutube.ru/video/private/62f1bf84116345a6ca84c96fe41d5f3b/?p=6-YF43xW9ueeR4JPwTvTGQ)** — видео защиты
- **[Плейлист на Rutube](https://rutube.ru/plst/1579769)** — плейлист
- **[Смотреть в VK Видео](https://vkvideo.ru/video-232514568_456239193)** — видео защиты
- **[Плейлист в VK Видео](https://vkvideo.ru/playlist/-232514568_41)** — плейлист
- **[Репозиторий на GitHub](https://github.com/Katerok27153/study_2025-2026_mathmod.git)** — репозиторий проекта
- **[Релиз на GitHub](https://github.com/Katerok27153/study_2025-2026_mathmod/releases/tag/v2.0.1)** — релиз проекта
- **[Репозиторий на GitVerse](https://gitverse.ru/Katerok27153/study_2025-2026_mathmod.git)** — репозиторий проекта
- **[Релиз на GitVerse](https://gitverse.ru/Katerok27153/study_2025-2026_mathmod/releases/tag/v2.0.1)** — релиз проекта
