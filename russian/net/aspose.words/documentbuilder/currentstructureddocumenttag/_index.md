---
title: DocumentBuilder.CurrentStructuredDocumentTag
linktitle: CurrentStructuredDocumentTag
articleTitle: CurrentStructuredDocumentTag
second_title: Aspose.Words для .NET
description: Откройте для себя свойство CurrentStructuredDocumentTag в DocumentBuilder. Легко получайте доступ к выбранному структурированному тегу документа для эффективного управления документами.
type: docs
weight: 80
url: /ru/net/aspose.words/documentbuilder/currentstructureddocumenttag/
---
## DocumentBuilder.CurrentStructuredDocumentTag property

Получает структурированный тег документа, который в данный момент выбран в этом[`DocumentBuilder`](../) .

```csharp
public StructuredDocumentTag CurrentStructuredDocumentTag { get; }
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

* class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
