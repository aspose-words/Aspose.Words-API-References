---
title: DocumentBuilder.InsertStructuredDocumentTag
linktitle: InsertStructuredDocumentTag
articleTitle: InsertStructuredDocumentTag
second_title: Aspose.Words для .NET
description: Легко улучшайте свои документы с помощью метода DocumentBuilder InsertStructuredDocumentTag. Легко добавляйте структурированные теги документов для лучшей организации!
type: docs
weight: 480
url: /ru/net/aspose.words/documentbuilder/insertstructureddocumenttag/
---
## DocumentBuilder.InsertStructuredDocumentTag method

Вставляет[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) в документ.

```csharp
public StructuredDocumentTag InsertStructuredDocumentTag(SdtType type)
```

### Возвращаемое значение

The[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) узел, который был только что вставлен.

## Примеры

Показывает, как просто вставить структурированный тег документа.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveTo(doc.FirstSection.Body.Paragraphs[3]);
// Обратите внимание, что для вставки разрешены только следующие типы StructuredDocumentTag:
// SdtType.PlainText, SdtType.RichText, SdtType.Checkbox, SdtType.DropDownList,
// SdtType.ComboBox, SdtType.Picture, SdtType.Date.
// Уровень разметки вставленного StructuredDocumentTag будет определен автоматически и зависит от позиции, в которую он вставляется.
// Добавленный StructuredDocumentTag унаследует форматирование абзаца и шрифта из позиции курсора.
StructuredDocumentTag sdtPlain = builder.InsertStructuredDocumentTag(SdtType.PlainText);

doc.Save(ArtifactsDir + "StructuredDocumentTag.InsertStructuredDocumentTag.docx");
```

### Смотрите также

* class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* enum [SdtType](../../../aspose.words.markup/sdttype/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
