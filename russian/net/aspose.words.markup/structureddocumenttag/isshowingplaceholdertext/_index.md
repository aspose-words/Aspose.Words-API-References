---
title: StructuredDocumentTag.IsShowingPlaceholderText
linktitle: IsShowingPlaceholderText
articleTitle: IsShowingPlaceholderText
second_title: Aspose.Words для .NET
description: Узнайте, как свойство IsShowingPlaceholderText в StructuredDocumentTag повышает ясность вашего документа, отделяя текст-заполнитель от обычного содержимого.
type: docs
weight: 150
url: /ru/net/aspose.words.markup/structureddocumenttag/isshowingplaceholdertext/
---
## StructuredDocumentTag.IsShowingPlaceholderText property

Указывает, является ли содержимое этого**СДТ** должно интерпретироваться как содержащее заполнитель text (в отличие от обычного текстового содержимого в SDT).

если установлено значение`истинный` , это состояние будет возобновлено (показ текста-заполнителя) при открытии этого документа.

```csharp
public bool IsShowingPlaceholderText { get; set; }
```

## Примеры

Показывает, как использовать содержимое стандартного блока в качестве пользовательского текста-заполнителя для структурированного тега документа.

```csharp
Document doc = new Document();

// Вставьте тег структурированного документа простого текста типа «PlainText», который будет функционировать как текстовое поле.
// По умолчанию будет отображаться подсказка «Нажмите здесь, чтобы ввести текст».
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Мы можем заставить тег отображать содержимое строительного блока вместо текста по умолчанию.
// Сначала добавьте строительный блок с содержимым в документ глоссария.
GlossaryDocument glossaryDoc = doc.GlossaryDocument;

BuildingBlock substituteBlock = new BuildingBlock(glossaryDoc);
substituteBlock.Name = "Custom Placeholder";
substituteBlock.AppendChild(new Section(glossaryDoc));
substituteBlock.FirstSection.AppendChild(new Body(glossaryDoc));
substituteBlock.FirstSection.Body.AppendParagraph("Custom placeholder text.");

glossaryDoc.AppendChild(substituteBlock);

// Затем используйте свойство "PlaceholderName" тега структурированного документа, чтобы сослаться на этот строительный блок по имени.
tag.PlaceholderName = "Custom Placeholder";

// Если «PlaceholderName» ссылается на существующий блок в документе глоссария родительского документа,
// мы сможем проверить строительный блок с помощью свойства «Placeholder».
Assert.AreEqual(substituteBlock, tag.Placeholder);

// Установите свойство "IsShowingPlaceholderText" в значение "true", чтобы обработать
// текущее содержимое структурированного тега документа как текст-заполнитель.
// Это означает, что при щелчке по текстовому полю в Microsoft Word будет немедленно выделено все содержимое тега.
// Установите свойство "IsShowingPlaceholderText" на "false", чтобы получить
// структурированный тег документа, чтобы обрабатывать его содержимое как текст, который уже ввел пользователь.
// При щелчке по этому тексту в Microsoft Word мигающий курсор будет установлен в месте щелчка.
tag.IsShowingPlaceholderText = isShowingPlaceholderText;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.PlaceholderBuildingBlock.docx");
```

### Смотрите также

* class [StructuredDocumentTag](../)
* пространство имен [Aspose.Words.Markup](../../../aspose.words.markup/)
* сборка [Aspose.Words](../../../)
