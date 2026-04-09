---
title: Этап 2. Модель колебаний цепочек. Алгоритм решения задачи о колебаниях цепочек

event: Групповой проект. Этап 2
event_url: 

location: РУДН
address:
  street: 
  city: Москва
  region:
  postcode:
  country: Россия

summary: Алгоритм численного моделирования колебаний одномерной цепочки связанных осцилляторов — семь ключевых этапов от задания параметров до визуализации результатов.
abstract: 'На втором этапе группового проекта описан алгоритм решения задачи моделирования колебаний одномерных цепочек. Рассмотрены семь ключевых этапов - задание параметров системы, настройка временной и пространственной дискретизации, инициализация системы, численное интегрирование уравнений движения (схема «чехарда»), анализ распределения энергии по нормальным модам через дискретное синус-преобразование, исследование ангармонических эффектов в задаче Ферми-Паста-Улама (FPU) и визуализация результатов.'

# Talk start and end times.
#   End time can optionally be hidden by prefixing the line with `#`.
date: '2026-04-09T13:00:00Z'
date_end: '2026-04-09T15:00:00Z'
all_day: false

# Schedule page publish date (NOT talk date).
publishDate: '2026-01-01T00:00:00Z'

authors: [mobyzova, eavernikovskaya, oskalashnikova, aabogatkina, ansusenko]
tags: ["численное моделирование", "Ферми-Паста-Улам", "колебания", "цепочка осцилляторов", "алгоритм", "схема чехарда"]

# Is this a featured talk? (true/false)
featured: false

image:
  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/bzdhc5b3Bxs)'
  focal_point: Right

url_code: ''
url_pdf: 'https://drive.google.com/file/d/1MVOcppY5sd-yH-0OkM14oBb1zJ1Y_vMp/view?usp=sharing'
url_slides: 'https://drive.google.com/file/d/1JtF1x5ad_eMQEO_-Jfe2J6rWdUQDsotH/view?usp=sharing'

# Custom links для двух видео
links:
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
На втором этапе проекта разработали и описали алгоритм численного решения задачи о колебаниях одномерной цепочки частиц. Алгоритм реализован в виде последовательности из семи шагов, готовых для программной реализации.

### Семь шагов алгоритма
1. **Задание параметров системы** — физические параметры (масса, жёсткость, число частиц, коэффициент ангармонизма) и начальные условия (смещения, скорости, тип возбуждения)
2. **Настройка временной и пространственной дискретизации** — выбор временного шага Δt с учётом условия устойчивости Куранта-Фридрихса-Леви (CFL)
3. **Инициализация системы** — задание равновесных координат и начальных смещений (например, в виде синусоиды для первой моды)
4. **Численное интегрирование уравнений движения** — явная конечно-разностная схема «чехарда» (leapfrog) с контролем сохранения полной энергии
5. **Анализ распределения энергии по модам** — дискретное синус-преобразование и вычисление энергии каждой нормальной моды
6. **Исследование ангармонических эффектов** — моделирование задачи Ферми-Паста-Улама: наблюдение квазипериодичности, возвратов и сверхпериодичности
7. **Визуализация результатов** — построение графиков смещений частиц, энергий мод во времени, анимаций колебаний и спектрограмм

### Основные результаты этапа
- Описан полный алгоритм моделирования от задания параметров до визуализации
- Выведены уравнения движения для гармонического и ангармонического случаев
- Приведена схема «чехарда» для интегрирования уравнений второго порядка
- Описан метод перехода в пространство нормальных мод через дискретное синус-преобразование
- Сформулированы критерии устойчивости и контроля точности (сохранение энергии)
- Выделены ключевые явления ангармонической цепочки: квазипериодичность, возврат Ферми-Паста-Улама, сверхпериодичность

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
