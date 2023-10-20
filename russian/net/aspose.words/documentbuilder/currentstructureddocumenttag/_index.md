---
title: DocumentBuilder.CurrentStructuredDocumentTag
linktitle: CurrentStructuredDocumentTag
articleTitle: CurrentStructuredDocumentTag
second_title: Aspose.Words для .NET
description: DocumentBuilder CurrentStructuredDocumentTag свойство. Получает тег структурированного документа выбранный в данный момент в этомDocumentBuilder  на С#.
type: docs
weight: 80
url: /ru/net/aspose.words/documentbuilder/currentstructureddocumenttag/
---
## DocumentBuilder.CurrentStructuredDocumentTag property

Получает тег структурированного документа, выбранный в данный момент в этом[`DocumentBuilder`](../) .

```csharp
public StructuredDocumentTag CurrentStructuredDocumentTag { get; }
```

## Примеры

Показывает, как переместить курсор DocumentBuilder внутри тега структурированного документа.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

// Существует несколько способов перемещения курсора:
// 1 - Переход к первому символу тега структурированного документа по индексу.
builder.MoveToStructuredDocumentTag(1, 1);

// 2 - Переход к первому символу тега структурированного документа по объекту.
StructuredDocumentTag tag = (StructuredDocumentTag)doc.GetChild(NodeType.StructuredDocumentTag, 2, true);
builder.MoveToStructuredDocumentTag(tag, 1);
builder.Write(" New text.");

Assert.AreEqual("R New text.ichText", tag.GetText().Trim());

// 3 - Переход к концу второго тега структурированного документа.
builder.MoveToStructuredDocumentTag(1, -1);
Assert.True(builder.IsAtEndOfStructuredDocumentTag);            

// Получить текущий выбранный тег структурированного документа.
builder.CurrentStructuredDocumentTag.Color = Color.Green;

doc.Save(ArtifactsDir + "Document.MoveToStructuredDocumentTag.docx");
```

### Смотрите также

* class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
