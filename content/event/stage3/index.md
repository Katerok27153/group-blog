---
title: Этап 3. Модель колебаний цепочек. Комплекс программ для решения задачи о колебаниях цепочек

event: Групповой проект. Этап 3
event_url: 

location: РУДН
address:
  street: 
  city: Москва
  region:
  postcode:
  country: Россия

summary: Разработан комплекс программ на Julia для моделирования гармонических и ангармонических цепочек, измерения собственных частот, анализа независимости мод и исследования задачи Ферми-Паста-Улама.
abstract: 'На третьем этапе группового проекта представлена программная реализация моделирования колебаний одномерных цепочек на языке Julia. Реализованы пять основных задач: моделирование гармонической цепочки со схемой «чехарда», измерение собственных частот нормальных мод с проверкой дисперсионного соотношения, анализ независимости мод через дискретное синус-преобразование (DST), моделирование цепочки с чередующимися массами (mlight = 1, mheavy = 2) и исследование ангармонической задачи Ферми-Паста-Улама (FPU) с наблюдением эффекта рекурренции энергии. Все программы протестированы и готовы к использованию в учебном процессе.'

# Talk start and end times.
#   End time can optionally be hidden by prefixing the line with `#`.
date: '2026-04-30T13:00:00Z'
date_end: '2026-04-30T15:00:00Z'
all_day: false

# Schedule page publish date (NOT talk date).
publishDate: '2026-01-01T00:00:00Z'

authors: [mobyzova, eavernikovskaya, oskalashnikova, aabogatkina, ansusenko]
tags: ["численное моделирование", "Ферми-Паста-Улам", "Julia", "гармоническая цепочка", "ангармоническая цепочка", "нормальные моды", "дискретное синус-преобразование", "FPU-возврат"]

# Is this a featured talk? (true/false)
featured: false

image:
  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/bzdhc5b3Bxs)'
  focal_point: Right

url_code: ''
url_pdf: 'https://drive.google.com/file/d/1RmWuQRH_DTpkUBbi06U9XcyT5nokR6ym/view?usp=sharing'
url_slides: 'https://drive.google.com/file/d/1wRPP96B8eEdxANnxC7ucvXSVnOzxa6B1/view?usp=sharing'

# Custom links для двух видео
links:
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
На третьем этапе разработан комплекс программ на языке Julia, реализующий численное моделирование колебаний одномерных цепочек частиц в гармоническом и ангармоническом приближениях.

### Пять реализованных задач
1. **Моделирование гармонической цепочки (task1.jl)**  
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
   - Наблюдение FPU-возврата (рекурренции энергии): концентрация энергии в низших модах и циклический возврат в первую моду

### Основные результаты этапа
- Разработаны 5 рабочих программ на Julia, прошедших тестирование
- Подтверждено дисперсионное соотношение для нормальных мод
- Экспериментально проверена независимость мод в линейном приближении
- Промоделирована цепочка с чередующимися массами
- Качественно воспроизведён классический эффект FPU-возврата, противоречащий интуиции термализации

### Параметры моделей
- Число частиц: 32
- Масса (гармоническая): 1
- Массы (чередующиеся): 1 (нечётные) / 2 (чётные)
- Жёсткость пружин: 1
- Коэффициент ангармонизма α: 0.5 (для FPU)
- Шаг по времени Δt: 0.01 (task1, task3, task5) / 0.001 (task2, task4)

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
