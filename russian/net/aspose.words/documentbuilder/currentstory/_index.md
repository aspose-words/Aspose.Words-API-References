---
title: DocumentBuilder.CurrentStory
linktitle: CurrentStory
articleTitle: CurrentStory
second_title: Aspose.Words для .NET
description: Откройте для себя свойство DocumentBuilder CurrentStory для эффективного доступа и управления выбранной историей, что улучшит ваши возможности редактирования документов.
type: docs
weight: 70
url: /ru/net/aspose.words/documentbuilder/currentstory/
---
## DocumentBuilder.CurrentStory property

Получает историю, которая в данный момент выбрана в этом[`DocumentBuilder`](../) .

```csharp
public Story CurrentStory { get; }
```

## Примеры

Показывает, как работать с текущей историей конструктора документов.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// История — это тип узла, который имеет дочерние узлы абзацев, такие как Тело.
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
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
