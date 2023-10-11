---
title: HtmlSaveOptions.ExportImagesAsBase64
second_title: Справочник по API Aspose.Words для .NET
description: HtmlSaveOptions свойство. Указывает сохраняются ли изображения в формате Base64 в выходной HTML MHTML или EPUB. Значение по умолчаниюЛОЖЬ .
type: docs
weight: 170
url: /ru/net/aspose.words.saving/htmlsaveoptions/exportimagesasbase64/
---
## HtmlSaveOptions.ExportImagesAsBase64 property

Указывает, сохраняются ли изображения в формате Base64 в выходной HTML, MHTML или EPUB. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool ExportImagesAsBase64 { get; set; }
```

### Примечания

Когда для этого свойства установлено значение`истинный` данные изображений экспортируются непосредственно в **изображение** элементы и отдельные файлы не создаются.

### Примеры

Показывает, как встроить шрифты в сохраненный HTML-документ.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlSaveOptions options = new HtmlSaveOptions
{
    ExportFontsAsBase64 = true,
    CssStyleSheetType = CssStyleSheetType.Embedded,
    PrettyFormat = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportFontsAsBase64.html", options);
```

Показывает, как сохранить документ .html со встроенными в него изображениями.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlSaveOptions options = new HtmlSaveOptions
{
    ExportImagesAsBase64 = exportImagesAsBase64,
    PrettyFormat = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportImagesAsBase64.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportImagesAsBase64.html");

Assert.True(exportImagesAsBase64
    ? outDocContents.Contains("<img src=\"data:image/png;base64")
    : outDocContents.Contains("<img src=\"HtmlSaveOptions.ExportImagesAsBase64.001.png\""));
```

### Смотрите также

* class [HtmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../htmlsaveoptions/)
* сборка [Aspose.Words](../../../)


