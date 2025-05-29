---
title: HtmlSaveOptions.ExportTextInputFormFieldAsText
linktitle: ExportTextInputFormFieldAsText
articleTitle: ExportTextInputFormFieldAsText
second_title: Aspose.Words для .NET
description: Узнайте, как свойство HtmlSaveOptions ExportTextInputFormFieldAsText оптимизирует поля формы ввода текста для бесшовного сохранения HTML или MHTML. Улучшите свой процесс экспорта!
type: docs
weight: 260
url: /ru/net/aspose.words.saving/htmlsaveoptions/exporttextinputformfieldastext/
---
## HtmlSaveOptions.ExportTextInputFormFieldAsText property

Управляет сохранением полей формы ввода текста в HTML или MHTML. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool ExportTextInputFormFieldAsText { get; set; }
```

## Примечания

При установке на`истинный` , экспортирует поля формы ввода текста как обычный текст. Когда`ЛОЖЬ`, экспортирует поля формы ввода текста Word как элементы INPUT в HTML.

При экспорте в EPUB поля формы ввода текста всегда сохраняются как text due в соответствии с требованиями этого формата.

## Примеры

Показывает, как указать папку для хранения связанных изображений после сохранения в формате .html.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

string imagesDir = Path.Combine(ArtifactsDir, "SaveHtmlWithOptions");

if (Directory.Exists(imagesDir))
    Directory.Delete(imagesDir, true);

Directory.CreateDirectory(imagesDir);

// Установите параметр для экспорта полей формы как обычного текста вместо элементов ввода HTML.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    ExportTextInputFormFieldAsText = true, 
    ImagesFolder = imagesDir
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

### Смотрите также

* class [HtmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
