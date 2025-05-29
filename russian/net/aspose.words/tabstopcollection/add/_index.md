---
title: TabStopCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words для .NET
description: Узнайте, как метод TabStopCollection Add эффективно добавляет или обновляет позиции табуляции, улучшая макет и форматирование вашего документа.
type: docs
weight: 30
url: /ru/net/aspose.words/tabstopcollection/add/
---
## Add(*[TabStop](../../tabstop/)*) {#add}

Добавляет или заменяет позицию табуляции в коллекции.

```csharp
public void Add(TabStop tabStop)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| tabStop | TabStop | Объект табуляции для добавления. |

## Примечания

Если в указанной позиции уже существует табуляция, она заменяется.

## Примеры

Показывает, как добавлять пользовательские позиции табуляции в документ.

```csharp
Document doc = new Document();
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// Ниже приведены два способа добавления позиций табуляции в коллекцию позиций табуляции абзаца с помощью свойства «ParagraphFormat».
// 1 — Создать объект «TabStop», а затем добавить его в коллекцию:
TabStop tabStop = new TabStop(ConvertUtil.InchToPoint(3), TabAlignment.Left, TabLeader.Dashes);
paragraph.ParagraphFormat.TabStops.Add(tabStop);

// 2 - Передать значения свойств новой позиции табуляции в метод "Добавить":
paragraph.ParagraphFormat.TabStops.Add(ConvertUtil.MillimeterToPoint(100), TabAlignment.Left,
    TabLeader.Dashes);

// Добавить табуляции на расстоянии 5 см ко всем абзацам.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true).OfType<Paragraph>())
{
    para.ParagraphFormat.TabStops.Add(ConvertUtil.MillimeterToPoint(50), TabAlignment.Left,
        TabLeader.Dashes);
}

// Каждый символ «табуляции» перемещает курсор конструктора в положение следующей позиции табуляции.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Start\tTab 1\tTab 2\tTab 3\tTab 4");

doc.Save(ArtifactsDir + "TabStopCollection.AddTabStops.docx");
```

### Смотрите также

* class [TabStop](../../tabstop/)
* class [TabStopCollection](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## Add(*double, [TabAlignment](../../tabalignment/), [TabLeader](../../tableader/)*) {#add_1}

Добавляет или заменяет позицию табуляции в коллекции.

```csharp
public void Add(double position, TabAlignment alignment, TabLeader leader)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| position | Double | Позиция (в пунктах), где следует добавить табуляцию. |
| alignment | TabAlignment | А[`TabAlignment`](../../tabalignment/) значение that определяет выравнивание текста на позиции табуляции. |
| leader | TabLeader | А[`TabLeader`](../../tableader/)значение that указывает тип линии выноски, отображаемой под символом табуляции. |

## Примечания

Если в указанной позиции уже существует табуляция, она заменяется.

## Примеры

Показывает, как добавлять пользовательские позиции табуляции в документ.

```csharp
Document doc = new Document();
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// Ниже приведены два способа добавления позиций табуляции в коллекцию позиций табуляции абзаца с помощью свойства «ParagraphFormat».
// 1 — Создать объект «TabStop», а затем добавить его в коллекцию:
TabStop tabStop = new TabStop(ConvertUtil.InchToPoint(3), TabAlignment.Left, TabLeader.Dashes);
paragraph.ParagraphFormat.TabStops.Add(tabStop);

// 2 - Передать значения свойств новой позиции табуляции в метод "Добавить":
paragraph.ParagraphFormat.TabStops.Add(ConvertUtil.MillimeterToPoint(100), TabAlignment.Left,
    TabLeader.Dashes);

// Добавить табуляции на расстоянии 5 см ко всем абзацам.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true).OfType<Paragraph>())
{
    para.ParagraphFormat.TabStops.Add(ConvertUtil.MillimeterToPoint(50), TabAlignment.Left,
        TabLeader.Dashes);
}

// Каждый символ «табуляции» перемещает курсор конструктора в положение следующей позиции табуляции.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Start\tTab 1\tTab 2\tTab 3\tTab 4");

doc.Save(ArtifactsDir + "TabStopCollection.AddTabStops.docx");
```

### Смотрите также

* enum [TabAlignment](../../tabalignment/)
* enum [TabLeader](../../tableader/)
* class [TabStopCollection](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
