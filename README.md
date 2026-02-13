# Лабораторная работа №9
## Адаптивная верстка: Медиа-запросы
**Цель работы:** Изучить принципы адаптивной верстки и медиа-запросов. В конце
создать адаптивную страницу портфолио, которая корректно отображается на всех устройствах.
#### Структура проекта:
- [файл README.md](README.md) 
- [сам.задание 1 (html)](flexbox-practice.html) 
- [сам.задание 1 (css)](nav-practice.css)
- [сам.задание 2 (html)](flexbox-practice.html)
- [сам.задание 2 (css)](flexbox-practice.css)
- [файл html](responsive.css) 
- [файл css](responsive.html)

### *Технологии и подходы*

#### 1. Flexbox (flexbox-practice.css)
Используется для:
- выравнивания заголовка и навигации в `header`,
- раскладки блоков в секции `.about`,
- центрирования и распределения пространства.

**Ключевые приёмы:**
- `display: flex` — включение Flexbox,
- `justify-content: space-between` — распределение элементов с промежутками,
- `align-items: center` — вертикальное выравнивание,
- `flex-wrap: wrap` — перенос элементов на новую строку,
- `flex: 1` — равное распределение ширины между элементами.

**Пример из кода:**
```css
.about {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: stretch;
    gap: 20px;
    flex-wrap: wrap;
}
.about p {
    flex: 1;
    min-width: 150px;
    max-width: 400px;
}
```
#### Media Адаптивность
Адаптация под:

- мобильные устройства (до 768px),
- планшеты (768–991px),
- десктопы (992px и выше),
- большие экраны (1200px+).

**Примеры:**
```css
.header {
    flex-direction: column;
}

@media (min-width: 768px) {
    .header {
        flex-direction: row;
        justify-content: space-between;
    }
    .nav {
        flex-direction: row;
    }
}

@media (min-width: 1200px) {
    .header, .footer {
        padding-left: calc((100% - 1200px) / 2);
        padding-right: calc((100% - 1200px) / 2);
    }
}
```

Aвтор: Горбачева М.А., группа ИСП-231