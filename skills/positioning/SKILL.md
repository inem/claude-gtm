---
name: positioning
description: "Слой 2.1 — категория, главная мысль, формулировка проблемы"
---

# Positioning

## Цель

Определить позиционирование продукта:
- Категория (mental model, не фича)
- Радикальная формулировка проблемы
- Дифференциатор
- Как люди должны о продукте говорить

## Входные данные

Прочитай `docs/gtm/context.yaml` — нужны:
- Продукт и конкуренты (discovery)
- Сегменты аудитории (audience)
- JTBD и боли (jtbd)

## Философия позиционирования

### Категория ≠ Фича

❌ "Chrome extension для сохранения фрагментов"
✅ "Personal knowledge layer для AI conversations"

❌ "Task manager"
✅ "Second brain for busy professionals"

Категория — это mental model. Как люди должны думать о продукте.

### Проблема должна быть радикальной

❌ "Неудобно искать в ChatGPT"
✅ "Ты теряешь интеллектуальный капитал каждый день"

❌ "Бардак в чатах"
✅ "ChatGPT — это одноразовый поток. Без системы ты сжигаешь ценные идеи."

Радикальная формулировка создаёт urgency.

### Дифференциатор — это not/but

❌ "Лучший X"
✅ "Not [категория конкурентов], but [новая категория]"

Пример:
> Not a chat exporter, but a knowledge refinery.
> Not a note-taking app, but a memory layer for AI.

## Процесс

### 1. Анализ (делаешь сам)

На основе собранных данных:

**Боли → Проблема**
- Какая боль самая интенсивная?
- Как сформулировать её радикально?
- Какие последствия если не решить?

**Конкуренты → Категория**
- В какой категории они все?
- Какую новую категорию можно создать?
- Как сдвинуть восприятие?

**JTBD → Ценность**
- Какой job самый важный?
- Какой результат обещаем?

### 2. Предложи варианты

Выдай пользователю 2-3 варианта позиционирования:

```markdown
## Варианты позиционирования

### Вариант A: [Название категории]

**Категория:** [Новая категория]

**Формулировка проблемы:**
> [Радикальная формулировка в 2-3 предложения]

**One-liner:** [Одно предложение]

**Дифференциатор:**
> Not [старая категория], but [новая категория].

**Как люди говорят:**
> "Я прогоняю всё через [Продукт]"
> "Это мой [метафора] для AI"

**Почему этот вариант:** [Обоснование]

---

### Вариант B: [Название категории]
...

---

### Вариант C: [Название категории]
...

---

**Моя рекомендация:** Вариант [X] потому что [причина].

Какой резонирует? Или миксуем?
```

### 3. Messaging Framework

После выбора варианта, создай messaging framework:

```markdown
## Messaging Framework

### Core Message
**One-liner:** [5-7 слов]
**Elevator pitch:** [2-3 предложения]
**Full description:** [1 абзац]

### Problem Statement
**Headline:** [Радикальная формулировка]
**Subhead:** [Последствия]
**Proof points:**
- [Статистика или факт]
- [Цитата из интервью]
- [Социальное доказательство]

### Value Proposition
**For** [целевая аудитория]
**Who** [проблема/ситуация]
**Product is** [категория]
**That** [ключевая выгода]
**Unlike** [конкуренты/альтернативы]
**Our product** [дифференциатор]

### Key Messages (для разных контекстов)
**Technical audience:** [версия для технарей]
**Business audience:** [версия для бизнеса]
**Casual/social:** [версия для соцсетей]

### Phrases to Use
- [Фраза 1]
- [Фраза 2]
- [Фраза 3]

### Phrases to Avoid
- [Антипаттерн 1]
- [Антипаттерн 2]
```

## Выходные данные

### context.yaml

```yaml
positioning:
  category: "Personal knowledge layer for AI conversations"

  problem:
    headline: "You're burning intellectual capital every day"
    radical_formulation: |
      ChatGPT generates value. Without a system to capture it,
      you're treating gold like garbage. Every insight you lose
      is work you'll repeat.
    consequences:
      - "Repeated work"
      - "Lost insights"
      - "No compound knowledge"

  differentiator:
    not_but: "Not a chat exporter, but a knowledge refinery"
    vs_competitors: |
      Exporters save everything (noise).
      We save what matters (signal).

  one_liner: "Distill knowledge from ChatGPT"

  how_people_talk:
    - "I run everything through Refinery"
    - "It's my memory layer for AI"

  messaging:
    elevator_pitch: |
      ...
    value_proposition: |
      ...
```

## Критерий завершения

- Определена категория (не фича)
- Сформулирована радикальная проблема
- Есть чёткий дифференциатор
- Создан messaging framework
- Пользователь подтвердил
