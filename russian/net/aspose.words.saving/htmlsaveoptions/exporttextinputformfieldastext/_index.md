---
title: HtmlSaveOptions.ExportTextInputFormFieldAsText
second_title: Справочник по API Aspose.Words для .NET
description: HtmlSaveOptions свойство. Управляет сохранением полей формы ввода текста в формате HTML или MHTML. Значение по умолчаниюЛОЖЬ .
type: docs
weight: 260
url: /ru/net/aspose.words.saving/htmlsaveoptions/exporttextinputformfieldastext/
---
## HtmlSaveOptions.ExportTextInputFormFieldAsText property

Управляет сохранением полей формы ввода текста в формате HTML или MHTML. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool ExportTextInputFormFieldAsText { get; set; }
```

### Примечания

Если установлено значение`истинный` , экспортирует поля формы ввода текста как обычный текст. Когда`ЛОЖЬ`, экспортирует поля формы ввода текста Word как элементы INPUT в HTML.

При экспорте в EPUB поля формы ввода текста всегда сохраняются как текст в соответствии с требованиями этого формата .

### Примеры

Показывает, как указать папку для хранения связанных изображений после сохранения в .html.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

string imagesDir = Path.Combine(ArtifactsDir, "SaveHtmlWithOptions");

if (Directory.Exists(imagesDir))
    Directory.Delete(imagesDir, true);

Directory.CreateDirectory(imagesDir);

// Установите опцию для экспорта полей формы в виде обычного текста вместо элементов ввода HTML.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    ExportTextInputFormFieldAsText = true, 
    ImagesFolder = imagesDir
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

### Смотрите также

* class [HtmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../htmlsaveoptions/)
* сборка [Aspose.Words](../../../)


