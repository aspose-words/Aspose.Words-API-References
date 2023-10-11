---
title: DocumentBuilder.CurrentStory
second_title: Справочник по API Aspose.Words для .NET
description: DocumentBuilder свойство. Получает историю выбранную в данный момент в этомDocumentBuilder .
type: docs
weight: 70
url: /ru/net/aspose.words/documentbuilder/currentstory/
---
## DocumentBuilder.CurrentStory property

Получает историю, выбранную в данный момент в этом[`DocumentBuilder`](../) .

```csharp
public Story CurrentStory { get; }
```

### Примеры

Показывает, как работать с текущей историей конструктора документов.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// История — это тип узла, у которого есть дочерние узлы «Абзац», например «Тело».
Assert.AreEqual(builder.CurrentStory, doc.FirstSection.Body);
Assert.AreEqual(builder.CurrentStory, builder.CurrentParagraph.ParentNode);
Assert.AreEqual(StoryType.MainText, builder.CurrentStory.StoryType);

builder.CurrentStory.AppendParagraph("Text added to current Story.");

// История также может содержать таблицы.
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1");
builder.InsertCell();
builder.Write("Row 1, cell 2");
builder.EndTable();

Assert.IsTrue(builder.CurrentStory.Tables.Contains(table));
```

### Смотрите также

* class [Story](../../story/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../documentbuilder/)
* сборка [Aspose.Words](../../../)


