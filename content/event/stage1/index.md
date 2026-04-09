---
title: Этап 1. Модель колебаний цепочек. Теоретическое описание задачи и модели

event: Групповой проект. Этап 1
event_url: 

location: РУДН
address:
  street: 
  city: Москва
  region:
  postcode:
  country: Россия

summary: Исследование колебаний в одномерной цепочке связанных осцилляторов — простейшей модели твердого тела (кристаллической решетки).
abstract: 'Первый этап проекта посвящен теоретическому описанию модели колебаний одномерной цепочки частиц, соединенных пружинками. Рассматриваются два случая: гармонический (линейные пружинки) и ангармонический (с нелинейной поправкой) — известная задача Ферми-Паста-Улама (FPU).'

# Talk start and end times.
#   End time can optionally be hidden by prefixing the line with `#`.
date: '2026-03-19T13:00:00Z'
date_end: '2026-03-19T15:00:00Z'
all_day: false

# Schedule page publish date (NOT talk date).
publishDate: '2026-01-01T00:00:00Z'

authors: [mobyzova, eavernikovskaya, oskalashnikova, aabogatkina, ansusenko]
tags: ["численное моделирование", "Ферми-Паста-Улам", "колебания", "цепочка осцилляторов"]

# Is this a featured talk? (true/false)
featured: false

image:
  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/bzdhc5b3Bxs)'
  focal_point: Right

url_code: ''
url_pdf: 'https://drive.google.com/file/d/1vw-zbtj4dFmlj5RDVqhjWZtXP4ILKiFz/view?usp=sharing'
url_slides: 'https://drive.google.com/file/d/1u2PSTe6sBN1n0FWqs0e_H0620vM1etoW/view?usp=sharing'

# Custom links для двух видео
links:
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
- **[Скачать презентацию (PDF)](https://drive.google.com/file/d/1u2PSTe6sBN1n0FWqs0e_H0620vM1etoW/view)** — слайды защиты
- **[Смотреть на Rutube](https://rutube.ru/video/private/075bd744719ff60ac52703e602b35d7d/?p=B8DrWpELk5VrhpLTxCYeZw)** — видео защиты
- **[Плейлист на Rutube](https://rutube.ru/plst/1542100)** — плейлист
- **[Смотреть в VK Видео](https://vkvideo.ru/video-232514568_456239153)** — видео защиты
- **[Плейлист в VK Видео](https://vkvideo.ru/playlist/-232514568_34)** — плейлист
- **[Репозиторий на GitHub](https://github.com/Katerok27153/study_2025-2026_mathmod.git)** — репозиторий проекта
- **[Релиз на GitHub](https://github.com/Katerok27153/study_2025-2026_mathmod/releases/tag/v1.0.1)** — релиз проекта
- **[Репозиторий на GitVerse](https://gitverse.ru/Katerok27153/study_2025-2026_mathmod.git)** — репозиторий проекта
- **[Релиз на GitVerse](https://gitverse.ru/Katerok27153/study_2025-2026_mathmod/releases/tag/v1.0.1)** — релиз проекта
