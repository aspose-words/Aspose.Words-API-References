---
title: StructuredDocumentTag.IsShowingPlaceholderText
linktitle: IsShowingPlaceholderText
articleTitle: IsShowingPlaceholderText
second_title: Aspose.Words для .NET
description: StructuredDocumentTag IsShowingPlaceholderText свойство. Указывает будет ли содержимое этогоСДТдолжно интерпретироваться как содержащее заполнитель text в отличие от обычного текстового содержимого в SDT на С#.
type: docs
weight: 150
url: /ru/net/aspose.words.markup/structureddocumenttag/isshowingplaceholdertext/
---
## StructuredDocumentTag.IsShowingPlaceholderText property

Указывает, будет ли содержимое этого**СДТ**должно интерпретироваться как содержащее заполнитель text (в отличие от обычного текстового содержимого в SDT).

, если установлено значение`истинный` , это состояние будет возобновлено (с отображением текста-заполнителя) при открытии этого документа.

```csharp
public bool IsShowingPlaceholderText { get; set; }
```

## Примеры

Показывает, как использовать содержимое стандартного блока в качестве пользовательского текста-заполнителя для тега структурированного документа.

```csharp
Document doc = new Document();

// Вставляем тег структурированного документа в виде обычного текста типа «PlainText», который будет функционировать как текстовое поле.
// Содержимое, которое будет отображаться по умолчанию: «Нажмите здесь, чтобы ввести текст». быстрый.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Мы можем заставить тег отображать содержимое строительного блока вместо текста по умолчанию.
// Сначала добавляем строительный блок с содержимым в документ глоссария.
GlossaryDocument glossaryDoc = doc.GlossaryDocument;

BuildingBlock substituteBlock = new BuildingBlock(glossaryDoc);
substituteBlock.Name = "Custom Placeholder";
substituteBlock.AppendChild(new Section(glossaryDoc));
substituteBlock.FirstSection.AppendChild(new Body(glossaryDoc));
substituteBlock.FirstSection.Body.AppendParagraph("Custom placeholder text.");

glossaryDoc.AppendChild(substituteBlock);

// Затем используйте свойство PlaceholderName тега структурированного документа, чтобы ссылаться на этот строительный блок по имени.
tag.PlaceholderName = "Custom Placeholder";

// Если «PlaceholderName» относится к существующему блоку в глоссарии родительского документа,
// мы сможем проверить строительный блок через свойство Placeholder.
Assert.AreEqual(substituteBlock, tag.Placeholder);

// Установите для свойства IsShowingPlaceholderText значение true, чтобы обрабатывать
// Текущее содержимое тега структурированного документа в виде текста-заполнителя.
// Это означает, что нажатие на текстовое поле в Microsoft Word немедленно выделит все содержимое тега.
// Установите для свойства IsShowingPlaceholderText значение «false», чтобы получить
// структурированный тег документа, который будет рассматривать его содержимое как текст, который уже ввел пользователь.
// При нажатии на этот текст в Microsoft Word мигающий курсор поместится в выбранное место.
tag.IsShowingPlaceholderText = isShowingPlaceholderText;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.PlaceholderBuildingBlock.docx");
```

### Смотрите также

* class [StructuredDocumentTag](../)
* пространство имен [Aspose.Words.Markup](../../../aspose.words.markup/)
* сборка [Aspose.Words](../../../)
