---
name: growth
description: "Этап 6 — growth loops, viral механики, механики распространения"
---

# Growth

## Цель

Не каналы (где постить), а механики (как один пользователь приводит другого).

Определить:
- Viral loops
- Share-механики
- Network effects
- Growth experiments

## Входные данные

Прочитай `docs/gtm/context.yaml` — нужны:
- Продукт (discovery)
- Аудитория и где обитают (audience)
- Позиционирование (positioning)
- Retention механики (retention)

## Философия growth

### Каналы ≠ Growth

❌ "Запостим в Reddit и Twitter"
✅ "Пользователь делится коллекцией → его друзья видят → устанавливают → делятся"

Каналы — это push (ты толкаешь).
Growth loops — это pull (продукт сам распространяется).

### Типы growth loops

**1. Viral Loop**
Пользователь приглашает других как часть использования.
> Dropbox: пригласи друга — получи место

**2. Content Loop**
Контент созданный пользователями привлекает новых.
> Pinterest: пины индексируются → SEO → новые пользователи

**3. Paid Loop**
Деньги → реклама → пользователи → деньги → больше рекламы.
> Facebook ads

**4. Sales Loop**
Revenue → salespeople → more revenue.
> Enterprise SaaS

### Для indie/small products

Обычно работает комбинация:
- **Organic content** (твой контент привлекает)
- **User-generated content** (пользователи создают привлекающий контент)
- **Word of mouth** (рассказывают друзьям)
- **Community** (активность в нишевых сообществах)

## Процесс

### 1. Анализ (делаешь сам)

На основе продукта определи:

**Что можно шарить?**
- Результаты работы
- Коллекции/списки
- Достижения
- Полезный контент

**Есть ли network effect?**
- Продукт лучше когда больше пользователей?
- Есть ли социальный компонент?

**Какой контент может создавать пользователь?**
- Что другие захотят увидеть?
- Что может индексироваться поиском?

### 2. Предложи growth механики

```markdown
## Growth Strategy

### Primary Growth Loop

```
[Триггер] → [Действие пользователя] → [Exposure] → [Новый пользователь] → [Триггер]
```

**Для [Продукт]:**
```
[Описание конкретного loop]
```

**Оценка силы:** [сильный/средний/слабый]
**Почему:** [обоснование]

### Share-механики

#### Что можно шарить

| Что | Куда | Ценность для получателя |
|-----|------|------------------------|
| [Элемент 1] | [Платформа] | [Почему интересно] |
| [Элемент 2] | [Платформа] | [Почему интересно] |

#### Как стимулировать sharing

- [Механика 1]
- [Механика 2]

### Word of Mouth

**Когда рассказывают о продукте:**
- [Ситуация 1]
- [Ситуация 2]

**Фразы которые хотим услышать:**
- "[Фраза 1]"
- "[Фраза 2]"

**Как усилить WoM:**
- [Тактика 1]
- [Тактика 2]

### Community-led Growth

**Где тусуется ЦА:**
- [Сообщество 1] — [размер, активность]
- [Сообщество 2] — [размер, активность]

**Стратегия присутствия:**
- [Не спам, а ценность — конкретно как]

### Content-led Growth

**Контент который привлекает ЦА:**
- [Тип контента 1]
- [Тип контента 2]

**SEO возможности:**
- [Ключевые запросы]

**User-generated content:**
- [Что пользователи могут создавать]
- [Как это привлекает новых]

### Growth Experiments (первые 3)

| Эксперимент | Гипотеза | Метрика успеха | Усилия |
|-------------|----------|----------------|--------|
| [Exp 1] | [Если X, то Y] | [Метрика > Z] | [Low/Med/High] |
| [Exp 2] | [Если X, то Y] | [Метрика > Z] | [Low/Med/High] |
| [Exp 3] | [Если X, то Y] | [Метрика > Z] | [Low/Med/High] |

### Честная оценка

**Сила organic growth:** [сильная/средняя/слабая]

**Если слабая:**
> ⚠️ Продукт не имеет сильного natural viral loop.
> Это нормально для многих продуктов. Значит нужно:
> - Больше усилий на acquisition
> - Или добавить share-механику в продукт
> - Или принять медленный рост

---

Это реалистично для твоего продукта? Что добавить?
```

### 3. Проверка на притянутость

Если viral loop притянут за уши — скажи честно:
- "Реальный viral coefficient будет ~0.1, это слабо"
- "Основной рост будет через X, не через вирусность"

## Выходные данные

### context.yaml

```yaml
growth:
  primary_loop:
    description: |
      User saves valuable collection →
      Shares as "My best ChatGPT prompts" →
      Friends see → Install → Save → Share
    strength: "medium"
    coefficient_estimate: "0.2-0.3"

  share_mechanics:
    - what: "Collections/boards"
      where: "Twitter, Reddit, LinkedIn"
      value: "Curated knowledge packs"
    - what: "Individual insights"
      where: "Social media"
      value: "Valuable standalone content"

  word_of_mouth:
    trigger_situations:
      - "Someone complains about losing ChatGPT insights"
      - "Discussion about AI productivity tools"
    desired_phrases:
      - "I use Refinery for that"
      - "Just save it to Refinery"
    amplification:
      - "Make sharing frictionless"
      - "Create shareable content formats"

  community:
    primary:
      - name: "r/ChatGPT"
        size: "2M+"
        strategy: "Helpful comments, occasional show-off posts"
      - name: "Twitter AI community"
        strategy: "Build in public, share insights"

  content:
    seo_keywords:
      - "save chatgpt conversations"
      - "organize chatgpt"
      - "chatgpt knowledge management"
    ugc_potential: |
      Public collections could be indexed,
      become destination for specific topics.

  experiments:
    - name: "Public collections"
      hypothesis: "If users can share collections publicly, 10% will"
      metric: "Collections shared / total collections > 10%"
      effort: "medium"

  assessment:
    organic_strength: "medium"
    primary_channel: "Community + Word of mouth"
    notes: |
      Not naturally viral, but shareable content exists.
      Growth will be steady, not explosive.
```

## Критерий завершения

- Определены реальные growth loops (не притянутые)
- Описаны share-механики
- Есть plan для community/content growth
- Сформулированы первые эксперименты
- Честная оценка силы organic growth
- Пользователь подтвердил
