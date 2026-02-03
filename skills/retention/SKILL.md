---
name: retention
description: "Этап 5 — retention, compound value, механики возврата"
---

# Retention

## Цель

Ответить на главный вопрос: **Почему пользователь вернётся через 2 недели?**

Без retention GTM — это просто шум. Определить:
- Compound value (что становится лучше со временем)
- Механики возврата
- Retention метрики

## Входные данные

Прочитай `docs/gtm/context.yaml` — нужны:
- Продукт (discovery)
- JTBD и боли (jtbd)
- Позиционирование (positioning)

## Философия retention

### Продукт должен компаундиться

❌ Продукт одинаково полезен в день 1 и день 100
✅ Продукт становится ценнее с каждым использованием

Примеры compound value:
- **Notion:** Чем больше заметок, тем ценнее база знаний
- **Spotify:** Чем больше слушаешь, тем лучше рекомендации
- **Slack:** Чем больше история, тем ценнее поиск

### Switching cost должен расти

Чем дольше используешь, тем сложнее уйти:
- Накопленные данные
- Настроенные workflows
- Привычки

### Триггеры возврата

Что заставляет открыть продукт снова:
- Внешний триггер (уведомление, email)
- Внутренний триггер (привычка, потребность)

## Процесс

### 1. Анализ (делаешь сам)

На основе продукта и JTBD определи:

**Что накапливается?**
- Данные
- Настройки
- Связи
- История

**Что улучшается со временем?**
- Персонализация
- Рекомендации
- Структура
- Понимание пользователя

**Какие естественные триггеры возврата?**
- Когда возникает потребность снова?
- Что напоминает о продукте?

### 2. Предложи retention механики

```markdown
## Retention Strategy

### Compound Value

**Что накапливается:**
- [Элемент 1] — [почему ценно]
- [Элемент 2] — [почему ценно]

**Что становится лучше:**
- День 1: [состояние]
- День 30: [состояние]
- День 90: [состояние]

**Switching cost:**
- После [X] использований уйти сложно потому что [причина]

### Механики возврата

#### Естественные триггеры
1. **[Триггер 1]**
   - Когда: [ситуация]
   - Действие: [что делает пользователь]

2. **[Триггер 2]**
   - Когда: [ситуация]
   - Действие: [что делает пользователь]

#### Искусственные триггеры (если нужны)
- [Email/уведомление и когда]
- [Напоминание и контекст]

### Retention Loops

```
[Действие] → [Ценность] → [Накопление] → [Больше ценности] → [Действие]
```

Пример для knowledge app:
```
Сохранил фрагмент → Нашёл позже → База растёт → Поиск ценнее → Сохраняешь больше
```

### Анти-churn механики

**Почему могут уйти:**
- [Причина 1]
- [Причина 2]

**Как предотвратить:**
- [Решение 1]
- [Решение 2]

### Метрики

| Метрика | Что измеряет | Цель |
|---------|--------------|------|
| D1 retention | Вернулись на след. день | >X% |
| D7 retention | Вернулись через неделю | >Y% |
| D30 retention | Вернулись через месяц | >Z% |
| [Продуктовая метрика] | [Описание] | [Цель] |

---

Это похоже на реальность твоего продукта? Что поправить?
```

### 3. Проверка на реалистичность

Задай себе (не пользователю):
- Есть ли реальный compound value или притянуто?
- Достаточно ли сильны триггеры возврата?
- Что если убрать искусственные триггеры — вернутся?

Если retention слабый — скажи честно:
> ⚠️ У продукта слабый natural retention. Это не killer, но нужно либо добавить compound value, либо смириться с высоким churn и компенсировать acquisition.

## Выходные данные

### context.yaml

```yaml
retention:
  compound_value:
    accumulates:
      - element: "Saved fragments"
        why_valuable: "Personal knowledge base grows"
      - element: "Collections/boards"
        why_valuable: "Organization improves"

    improves_over_time:
      day_1: "Empty, learning interface"
      day_30: "50+ fragments, finding value in search"
      day_90: "Personal knowledge system, can't live without"

    switching_cost: |
      After 100+ saved fragments, migrating to another tool
      means losing curated knowledge base.

  triggers:
    natural:
      - situation: "Found something valuable in ChatGPT"
        action: "Cmd+Shift+S to save"
      - situation: "Need to find something saved"
        action: "Open Refinery search"

    artificial:
      - type: "Weekly digest"
        when: "Monday morning"
        content: "Your saved insights this week"

  loops:
    description: |
      Save fragment → Find it later → Value proven →
      Save more → Better search → Save more

  anti_churn:
    reasons:
      - "Forgot about it"
      - "Not enough saved to be valuable"
    prevention:
      - "Gentle reminder after 3 days of no saves"
      - "Show value: 'You saved X insights this month'"

  metrics:
    - name: "D1 retention"
      target: "40%"
    - name: "D7 retention"
      target: "25%"
    - name: "Fragments per active user"
      target: "5+/week"

  assessment:
    strength: "medium"
    notes: |
      Natural retention exists but not super strong.
      Needs habit formation period.
```

## Критерий завершения

- Определён compound value
- Описаны механики возврата
- Установлены retention метрики
- Честная оценка силы retention
- Пользователь подтвердил
