# claude-gtm

Go-To-Market стратегия в трёх слоях.

## Философия

**Не анкета, а аналитик.**
Claude сам делает ресёрч, приходит с гипотезами — ты только валидируешь.

**Три слоя, не каша.**
Каждый слой — отдельная цель, отдельный документ. Нельзя смешивать.

## Три слоя

### Слой 1: Product Loop
**Цель:** Формируется ли привычка?

- Discovery — ресёрч рынка и конкурентов
- Audience — сегменты ЦА
- JTBD — эмуляция интервью, боли, jobs
- Retention — compound value, механики возврата

→ `docs/gtm/product-loop.md`

### Слой 2: Messaging
**Цель:** Одна мысль, повторённая 50 раз

- Positioning — категория, главная мысль
- Messaging — вариации подачи, phrases

→ `docs/gtm/messaging.md`

### Слой 3: Distribution
**Цель:** 20 правильных людей для проверки

- Distribution — каналы, тактика 0-100 юзеров
- Launch — первые шаги

→ `docs/gtm/distribution.md`

### Финал: Critique
Самокритика всех трёх слоёв.

## Установка

```bash
# Вариант 1: Через plugin marketplace
/plugin marketplace add inem/claude-gtm
/plugin install claude-gtm@claude-gtm-marketplace

# Вариант 2: Напрямую в skills
git clone https://github.com/inem/claude-gtm.git
cp -r claude-gtm/skills/* ~/.claude/skills/
```

## Использование

### Полный цикл
```
/gtm
```

### Отдельные слои
```
/gtm:product      — Product Loop
/gtm:messaging    — Messaging
/gtm:distribution — Distribution
```

### Отдельные этапы
```
/discovery      — ресёрч рынка
/audience       — сегменты ЦА
/jtbd           — интервью и боли
/retention      — compound value
/positioning    — категория и главная мысль
/messaging      — вариации подачи
/distribution   — тактика 0-100
/launch         — первые шаги
/critique       — самокритика
```

## Результаты

```
docs/gtm/
├── context.yaml        # Вся информация
├── product-loop.md     # Слой 1
├── messaging.md        # Слой 2
├── distribution.md     # Слой 3
└── research/
    ├── competitors.md
    └── interviews.md
```

## Важно

- **Product Loop первый** — без двигателя колёса бессмысленны
- **Messaging служит продукту** — не наоборот
- **Distribution — лаборатория** — не рост, а проверка гипотез
- **Рост после** — когда люди возвращаются сами

## Лицензия

MIT
