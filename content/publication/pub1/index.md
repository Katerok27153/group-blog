 ---
title: 'Этап 1. Модель колебаний цепочек. Теоретическое описание задачи и модели. Публикация'

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
publishDate: '2026-03-19T00:00:00Z'

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ['paper-conference']

# Publication name and optional abbreviated publication name.
publication: In *Групповой проект. Математическое моделирование, РУДН*
publication_short: In *ГП РУДН*

abstract: На первом этапе группового проекта выполнено теоретическое описание модели колебаний одномерной цепочки частиц, соединенных пружинками. Рассмотрены два случая - гармонический (линейные пружинки по закону Гука) и ангармонический (с нелинейной поправкой) — известная задача Ферми-Паста-Улама (FPU). Выведены уравнения движения, получено дисперсионное соотношение, описаны нормальные моды колебаний. Подготовлен численный алгоритм для следующих этапов исследования.

# Summary. An optional shortened abstract.
summary: Теоретическое описание модели колебаний цепочки осцилляторов. Гармонический и ангармонический случаи, задача Ферми-Паста-Улама.

tags: ["Численное Моделирование", "Ферми-Паста-Улам", "Колебания", "Цепочка Осцилляторов"]

# Display this page in the Featured widget?
featured: true

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_code: ''
url_pdf: 'https://drive.google.com/file/d/1vw-zbtj4dFmlj5RDVqhjWZtXP4ILKiFz/view?usp=sharing'
url_slides: 'https://drive.google.com/file/d/1u2PSTe6sBN1n0FWqs0e_H0620vM1etoW/view?usp=sharing'

# Custom links для двух видео
links:
  - name: Slides
    url: 'https://drive.google.com/file/d/1u2PSTe6sBN1n0FWqs0e_H0620vM1etoW/view?usp=sharing'
  - name: Rutube
    url: 'https://rutube.ru/video/private/075bd744719ff60ac52703e602b35d7d/?p=B8DrWpELk5VrhpLTxCYeZw'
    icon_pack: fab
    icon: rutube
  - name: VK Видео
    url: 'https://vkvideo.ru/video-232514568_456239153'
    icon_pack: fab
    icon: vk
  - name: GitHub
    url: 'https://github.com/Katerok27153/study_2025-2026_mathmod.git'
    icon_pack: fab
    icon: github
  - name: Релиз на GitHub
    url: 'https://github.com/Katerok27153/study_2025-2026_mathmod/releases/tag/v1.0.1'
    icon_pack: fas
    icon: download
  - name: GitVerse
    url: 'https://gitverse.ru/Katerok27153/study_2025-2026_mathmod.git'
    icon_pack: fab
    icon: git
  - name: Релиз на GitVerse
    url: 'https://gitverse.ru/Katerok27153/study_2025-2026_mathmod/releases/tag/v1.0.1'
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
На первом этапе проекта выполнили теоретическое описание модели колебаний одномерной цепочки частиц, соединенных пружинками. Это простейшая модель твердого тела (кристаллической решетки).

### Две модели
1. **Гармоническая** — пружинки подчиняются закону Гука (линейный случай)
2. **Ангармоническая** — добавлена нелинейная поправка (задача Ферми-Паста-Улама)

### Основные результаты этапа
- Вывели уравнения движения для цепочки частиц
- Получили дисперсионное соотношение и описали нормальные моды колебаний
- Рассмотрели ангармонический случай и сформулировали задачу Ферми-Паста-Улама
- Описали численный алгоритм (схема «чехарда» для интегрирования уравнений)
- Подготовили метод анализа распределения энергии по модам через дискретное преобразование Фурье

### Параметры модели
- Число частиц: 32 (как в оригинальном расчете FPU)
- Масса частицы: 1
- Жесткость пружин: 1
- Равновесное расстояние: 1
- Коэффициент ангармонизма: 0.1

## Материалы проекта

- **[Скачать отчёт (PDF)](https://drive.google.com/file/d/1vw-zbtj4dFmlj5RDVqhjWZtXP4ILKiFz/view?usp=sharing)** — полное теоретическое описание
- **[Скачать презентацию (PDF)](https://drive.google.com/file/d/1u2PSTe6sBN1n0FWqs0e_H0620vM1etoW/view?usp=sharing)** — слайды защиты
- **[Смотреть на Rutube](https://rutube.ru/video/private/075bd744719ff60ac52703e602b35d7d/?p=B8DrWpELk5VrhpLTxCYeZw)** — видео защиты
- **[Плейлист на Rutube](https://rutube.ru/plst/1542100)** — плейлист
- **[Смотреть в VK Видео](https://vkvideo.ru/video-232514568_456239153)** — видео защиты
- **[Плейлист в VK Видео](https://vkvideo.ru/playlist/-232514568_34)** — плейлист
- **[Репозиторий на GitHub](https://github.com/Katerok27153/study_2025-2026_mathmod.git)** — репозиторий проекта
- **[Релиз на GitHub](https://github.com/Katerok27153/study_2025-2026_mathmod/releases/tag/v1.0.1)** — релиз проекта
- **[Репозиторий на GitVerse](https://gitverse.ru/Katerok27153/study_2025-2026_mathmod.git)** — репозиторий проекта
- **[Релиз на GitVerse](https://gitverse.ru/Katerok27153/study_2025-2026_mathmod/releases/tag/v1.0.1)** — релиз проекта
