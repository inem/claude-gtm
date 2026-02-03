---
name: messaging
description: "Слой 2.2 — вариации подачи, phrases, категориальное внушение"
---

# Messaging

## Цель

Не контент-план. Категориальное внушение.

Одна мысль, повторённая 50 раз под разными углами.

## Входные данные

Прочитай `docs/gtm/context.yaml` — нужны:
- Positioning (главная категория и мысль)
- JTBD и боли (на каком языке говорит аудитория)
- Аудитория (где они, что резонирует)

## Философия

### Не фичи. Не обновления. Одна ось.

❌ "Мы добавили новую функцию X"
❌ "5 причин попробовать наш продукт"
❌ "Обзор возможностей"

✅ Одна концепция, поданная снова и снова:
- Под разными углами
- В разных форматах
- Для разных контекстов

### Пример для Refinery

Главная мысль:
> ChatGPT — генерация. Refinery — дистилляция.

Вариации этой оси:
- Потеря инсайтов
- Интеллектуальный капитал
- Вторая фаза работы с AI
- Memory layer
- Архив мышления
- Дистилляция разговора

Каждый пост, демо, скриншот — вариация этой оси.

## Процесс

### 1. Определи главную ось

На основе positioning сформулируй:

**Главная мысль (одно предложение):**
> [Проблема] → [Решение как категория]

**Контраст:**
> [Что есть сейчас] vs [Что даёт продукт]

### 2. Сгенерируй вариации

```markdown
## Вариации главной мысли

### Угол 1: [Название]
**Идея:** [Описание угла]
**Пример фразы:** "[Фраза]"
**Где использовать:** [Контекст]

### Угол 2: [Название]
**Идея:** [Описание угла]
**Пример фразы:** "[Фраза]"
**Где использовать:** [Контекст]

### Угол 3: [Название]
...

(минимум 5-7 вариаций)
```

### 3. Phrases to Use

```markdown
## Словарь продукта

### Использовать
- "[Фраза 1]" — [почему работает]
- "[Фраза 2]" — [почему работает]
- "[Фраза 3]" — [почему работает]

### Избегать
- "[Фраза 1]" — [почему не работает]
- "[Фраза 2]" — [почему не работает]

### Метафоры
- [Метафора 1]: [объяснение]
- [Метафора 2]: [объяснение]
```

### 4. Форматы подачи

```markdown
## Как подавать

### Текст (посты, комментарии)
- Формат: [описание]
- Пример: [пример]

### Визуал (GIF, скриншоты)
- Что показывать: [описание]
- Пример: [описание демо]

### Видео (если применимо)
- Формат: [описание]
- Длина: [секунды]

### Ответы на вопросы
- Когда спрашивают "[вопрос]" — отвечать "[ответ]"
```

### 5. Покажи пользователю

```markdown
## Messaging Strategy

### Главная ось
> [Одно предложение]

### Контраст
[Что есть] → [Что даём]

### 7 вариаций подачи
1. [Угол + фраза]
2. [Угол + фраза]
...

### Словарь
**Использовать:** [топ 5 фраз]
**Избегать:** [топ 3 антипаттерна]

### Форматы
- Текст: [формат]
- Визуал: [формат]

---

Это резонирует? Какие углы добавить/убрать?
```

## Выходные данные

### context.yaml

```yaml
messaging:
  core_axis: "ChatGPT generates. Refinery distills."

  contrast:
    before: "One-time conversations, lost insights"
    after: "Accumulated knowledge, searchable archive"

  variations:
    - angle: "Loss framing"
      idea: "Focus on what you're losing without the product"
      phrase: "Every insight you lose is work you'll repeat"
      context: "Problem-aware audiences"

    - angle: "Capital framing"
      idea: "Ideas as valuable assets"
      phrase: "Stop burning intellectual capital"
      context: "Business/productivity audiences"

    - angle: "Phase framing"
      idea: "Two-phase AI workflow"
      phrase: "Generation is phase 1. Distillation is phase 2."
      context: "Power users, workflow discussions"

  phrases:
    use:
      - phrase: "Distill knowledge"
        why: "Active verb, clear value"
      - phrase: "Memory layer"
        why: "Creates new category"

    avoid:
      - phrase: "Save your chats"
        why: "Sounds like backup, not value creation"
      - phrase: "Organize conversations"
        why: "Boring utility framing"

  metaphors:
    - name: "Refinery"
      meaning: "Crude oil → valuable fuel. Raw chats → valuable insights."
    - name: "Second brain"
      meaning: "External memory for AI conversations"

  formats:
    text: "Short, punchy. Lead with problem or contrast."
    visual: "GIF showing highlight → save → find later"
    video: "10-15 sec demo of core loop"
```

### docs/gtm/messaging.md

Полный messaging документ с примерами для каждого формата.

## Критерий завершения

- Определена главная ось (одна мысль)
- Сгенерированы 5-7 вариаций
- Составлен словарь phrases
- Определены форматы подачи
- Пользователь подтвердил что резонирует
