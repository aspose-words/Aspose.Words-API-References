---
title: SaveOptions.UpdateSdtContent
second_title: Справочник по API Aspose.Words для .NET
description: SaveOptions свойство. Получает или задает значение определяющее будет ли содержимоеStructuredDocumentTag обновляется перед сохранением.
type: docs
weight: 200
url: /ru/net/aspose.words.saving/saveoptions/updatesdtcontent/
---
## SaveOptions.UpdateSdtContent property

Получает или задает значение, определяющее, будет ли содержимое[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) обновляется перед сохранением.

```csharp
public bool UpdateSdtContent { get; set; }
```

### Примечания

Значение по умолчанию:`истинный` .

### Примеры

Показывает, как обновлять теги структурированного документа при сохранении документа в формате PDF.

```csharp
Document doc = new Document();

// Вставить тег структурированного документа раскрывающегося списка.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.DropDownList, MarkupLevel.Block);
tag.ListItems.Add(new SdtListItem("Value 1"));
tag.ListItems.Add(new SdtListItem("Value 2"));
tag.ListItems.Add(new SdtListItem("Value 3"));

// В раскрывающемся списке в настоящее время отображается «Выбрать элемент» в качестве текста по умолчанию.
// Установите свойство "SelectedValue" в один из элементов списка, чтобы получить тег
// отображаем значение этого элемента списка вместо текста по умолчанию.
tag.ListItems.SelectedValue = tag.ListItems[1];

doc.FirstSection.Body.AppendChild(tag);

// Создаем объект "PdfSaveOptions" для передачи в метод "Сохранить" документа
// для изменения того, как этот метод сохраняет документ в формате .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Установите для свойства "UpdateSdtContent" значение "false", чтобы не обновлять теги структурированного документа
// при сохранении документа в PDF. Они будут отображать свои значения по умолчанию, как они были во время строительства.
// Установите для свойства «UpdateSdtContent» значение «true», чтобы теги отображали обновленные значения в PDF-файле.
options.UpdateSdtContent = updateSdtContent;

doc.Save(ArtifactsDir + "StructuredDocumentTag.UpdateSdtContent.pdf", options);
```

### Смотрите также

* class [SaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../saveoptions/)
* сборка [Aspose.Words](../../../)


