---
title: DocumentBuilder.IsAtEndOfStructuredDocumentTag
linktitle: IsAtEndOfStructuredDocumentTag
articleTitle: IsAtEndOfStructuredDocumentTag
second_title: Aspose.Words для .NET
description: Откройте для себя свойство IsAtEndOfStructuredDocumentTag в DocumentBuilder — проверьте, находится ли курсор в конце структурированного тега документа для эффективного редактирования!
type: docs
weight: 120
url: /ru/net/aspose.words/documentbuilder/isatendofstructureddocumenttag/
---
## DocumentBuilder.IsAtEndOfStructuredDocumentTag property

Возврат**истинный** если курсор находится в конце структурированного документа тег.

```csharp
public bool IsAtEndOfStructuredDocumentTag { get; }
```

## Примеры

Показывает, как перемещать курсор DocumentBuilder внутри структурированного тега документа.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

// Существует несколько способов перемещения курсора:
// 1 - Перейти к первому символу структурированного тега документа по индексу.
builder.MoveToStructuredDocumentTag(1, 1);

// 2 - Перейти к первому символу структурированного тега документа по объекту.
StructuredDocumentTag tag = (StructuredDocumentTag)doc.GetChild(NodeType.StructuredDocumentTag, 2, true);
builder.MoveToStructuredDocumentTag(tag, 1);
builder.Write(" New text.");

Assert.AreEqual("R New text.ichText", tag.GetText().Trim());

// 3 — Перейти к концу второго структурированного тега документа.
builder.MoveToStructuredDocumentTag(1, -1);
Assert.True(builder.IsAtEndOfStructuredDocumentTag);

// Получить текущий выбранный структурированный тег документа.
builder.CurrentStructuredDocumentTag.Color = Color.Green;

doc.Save(ArtifactsDir + "Document.MoveToStructuredDocumentTag.docx");
```

### Смотрите также

* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
