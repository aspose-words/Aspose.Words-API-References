---
title: DocumentBuilder.IsAtEndOfStructuredDocumentTag
linktitle: IsAtEndOfStructuredDocumentTag
articleTitle: IsAtEndOfStructuredDocumentTag
second_title: Aspose.Words для .NET
description: DocumentBuilder IsAtEndOfStructuredDocumentTag свойство. Возвращаетистинный если курсор находится в конце тега структурированного документа на С#.
type: docs
weight: 120
url: /ru/net/aspose.words/documentbuilder/isatendofstructureddocumenttag/
---
## DocumentBuilder.IsAtEndOfStructuredDocumentTag property

Возвращает**истинный** если курсор находится в конце тега структурированного документа.

```csharp
public bool IsAtEndOfStructuredDocumentTag { get; }
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

* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
