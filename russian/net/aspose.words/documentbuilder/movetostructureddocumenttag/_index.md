---
title: DocumentBuilder.MoveToStructuredDocumentTag
linktitle: MoveToStructuredDocumentTag
articleTitle: MoveToStructuredDocumentTag
second_title: Aspose.Words для .NET
description: Легко переходите к структурированным тегам документа с помощью метода MoveToStructuredDocumentTag в DocumentBuilder, повышая эффективность редактирования документов.
type: docs
weight: 620
url: /ru/net/aspose.words/documentbuilder/movetostructureddocumenttag/
---
## MoveToStructuredDocumentTag(*int, int*) {#movetostructureddocumenttag_1}

Перемещает курсор на структурированный тег документа в текущем разделе.

```csharp
public void MoveToStructuredDocumentTag(int structuredDocumentTagIndex, int characterIndex)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| structuredDocumentTagIndex | Int32 | Индекс структурированного тега документа, к которому необходимо перейти. |
| characterIndex | Int32 | Индекс символа внутри структурированного тега документа. Отрицательное значение позволяет указать позицию от конца структурированного тега документа. Используйте -1, чтобы переместиться в конец структурированного тега документа. Если структурированный тег документа находится на уровне блока, и вы хотите переместить курсор в конец его последнего абзаца, укажите -2. |

## Примечания

Навигация осуществляется внутри текущей истории текущего раздела. То есть, если вы переместили курсор the на основной заголовок первого раздела, то*structuredDocumentTagIndex* указывает индекс структурированного тега документа внутри заголовка данного раздела.

Когда*structuredDocumentTagIndex* больше или равно 0, он указывает index с начала раздела, где 0 — первый структурированный тег документа. When *structuredDocumentTagIndex*меньше 0, он указывает индекс с конца раздела the , где -1 является последним структурированным тегом документа.

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

---

## MoveToStructuredDocumentTag(*[StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/), int*) {#movetostructureddocumenttag}

Перемещает курсор к тегу структурированного документа.

```csharp
public void MoveToStructuredDocumentTag(StructuredDocumentTag structuredDocumentTag, 
    int characterIndex)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| structuredDocumentTag | StructuredDocumentTag | Структурированный тег документа, к которому необходимо перейти. |
| characterIndex | Int32 | Индекс символа внутри структурированного тега документа. Отрицательное значение позволяет указать позицию от конца структурированного тега документа. Используйте -1, чтобы переместиться в конец структурированного тега документа. Если структурированный тег документа находится на уровне блока, и вы хотите переместить курсор в конец его последнего абзаца, укажите -2. |

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
