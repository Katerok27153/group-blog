---
title: Завершен третий этап группового проекта "Модель колебаний цепочек"
date: 2026-04-30
image:
  focal_point: 'top'
authors: [mobyzova, eavernikovskaya, oskalashnikova, aabogatkina, ansusenko]

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
---

Поздравляем нашу команду с завершением третьего этапа группового проекта "Модель колебаний цепочек"! Разработан комплекс программ на Julia для моделирования гармонических и ангармонических цепочек.

<!--more-->

На третьем этапе мы разработали пять программ на языке Julia, полностью реализующих алгоритм, описанный на втором этапе. Все программы протестированы и готовы к использованию.

**Пять реализованных программ:**

- **1. Гармоническая цепочка (task1.jl)**
	- Численное интегрирование схемы «чехарда» (leapfrog)
	- Параметры: N = 32, m = 1, k = 1, Δt = 0.01, T = 100
	- Начальное условие — первая нормальная мода

- **2. Измерение собственных частот (task2.jl)**
	- Определение частоты по пересечениям нуля
	- Сравнение с теоретическим дисперсионным соотношением
	- Результат: для чётных мод отклонение < 1%, что подтверждает корректность реализации

- **3. Анализ независимости нормальных мод (task3.jl)**
	- Дискретное синус-преобразование (DST) с ортонормировкой
	- Вычисление энергии первых пяти мод
	- Результат: в гармоническом случае энергия не перетекает между модами

- **4. Цепочка с чередующимися массами (task4.jl)**
	- m_light = 1 (нечётные), m_heavy = 2 (чётные)
	- Моделирование бинарной кристаллической структуры (типа NaCl)
	- Индивидуальное ускорение для каждой частицы

- **5. Ангармоническая цепочка. Задача Ферми-Паста-Улама (task5.jl)**
	- Кубическая нелинейность: α = 0.5
	- Метод Velocity Verlet
	- Результат: наблюдается классический FPU-возврат (рекурренция энергии)

**Основные результаты этапа:**
- Разработаны 5 рабочих программ на Julia, прошедших тестирование
- Подтверждено дисперсионное соотношение для нормальных мод (отклонение < 1% для чётных мод)
- Экспериментально проверена независимость мод в линейном приближении
- Промоделирована цепочка с чередующимися массами (аналог NaCl)
- Качественно воспроизведён классический эффект FPU-возврата — энергия не термализуется, а концентрируется в низших модах и циклически возвращается в первую моду


**Параметры моделей:**
| Параметр | Значение |
|----------|----------|
| Число частиц | 32 |
| Масса (гармоническая) | 1 |
| Массы (чередующиеся) | 1 (нечётные) / 2 (чётные) |
| Жёсткость пружин | 1 |
| Коэффициент ангармонизма α | 0.5 (для FPU) |
| Шаг по времени Δt | 0.01 (task1, task3, task5) / 0.001 (task2, task4) |

**Что дальше?**  
Следующие этапы проекта — анализ масштабируемости алгоритмов, оптимизация производительности и, возможно, расширение на двумерные модели.

Следите за нашими новостями! Будем публиковать результаты численных экспериментов и графики.

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
