---
title: DocumentBuilder.MoveToStructuredDocumentTag
linktitle: MoveToStructuredDocumentTag
articleTitle: MoveToStructuredDocumentTag
second_title: Aspose.Words для .NET
description: DocumentBuilder MoveToStructuredDocumentTag метод. Перемещает курсор на тег структурированного документа в текущем разделе на С#.
type: docs
weight: 580
url: /ru/net/aspose.words/documentbuilder/movetostructureddocumenttag/
---
## MoveToStructuredDocumentTag(*int, int*) {#movetostructureddocumenttag_1}

Перемещает курсор на тег структурированного документа в текущем разделе.

```csharp
public void MoveToStructuredDocumentTag(int structuredDocumentTagIndex, int characterIndex)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| structuredDocumentTagIndex | Int32 | Индекс тега структурированного документа, к которому необходимо перейти. |
| characterIndex | Int32 | Индекс символа внутри тега структурированного документа. Отрицательное значение позволяет указать позицию от конца тега структурированного документа. Используйте -1 to для перехода в конец тега структурированного документа. Если тег структурированного документа находится на уровне блока и вы хотите переместить курсор в конец его последнего абзаца, укажите -2. |

## Примечания

Навигация осуществляется внутри текущей истории текущего раздела. То есть, если вы переместили курсор в основной заголовок первого раздела, то*structuredDocumentTagIndex* указал индекс тега структурированного документа внутри этого заголовка этого раздела.

Когда*structuredDocumentTagIndex* больше или равно 0, он указывает index с начала раздела, где 0 является первым тегом структурированного документа. When *structuredDocumentTagIndex* меньше 0, он указывает индекс с конца раздела the , где -1 — это последний тег структурированного документа.

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

---

## MoveToStructuredDocumentTag(*[StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/), int*) {#movetostructureddocumenttag}

Перемещает курсор к тегу структурированного документа.

```csharp
public void MoveToStructuredDocumentTag(StructuredDocumentTag structuredDocumentTag, 
    int characterIndex)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| structuredDocumentTag | StructuredDocumentTag | Тег структурированного документа, к которому необходимо перейти. |
| characterIndex | Int32 | Индекс символа внутри тега структурированного документа. Отрицательное значение позволяет указать позицию от конца тега структурированного документа. Используйте -1 to для перехода в конец тега структурированного документа. Если тег структурированного документа находится на уровне блока и вы хотите переместить курсор в конец его последнего абзаца, укажите -2. |

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
