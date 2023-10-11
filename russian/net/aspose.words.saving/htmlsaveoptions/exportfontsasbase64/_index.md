---
title: HtmlSaveOptions.ExportFontsAsBase64
second_title: Справочник по API Aspose.Words для .NET
description: HtmlSaveOptions свойство. Указывает должны ли ресурсы шрифтов быть встроены в HTML в кодировке Base64. Значение по умолчаниюЛОЖЬ .
type: docs
weight: 150
url: /ru/net/aspose.words.saving/htmlsaveoptions/exportfontsasbase64/
---
## HtmlSaveOptions.ExportFontsAsBase64 property

Указывает, должны ли ресурсы шрифтов быть встроены в HTML в кодировке Base64. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool ExportFontsAsBase64 { get; set; }
```

### Примечания

По умолчанию шрифты записываются в отдельные файлы. Если для этой опции установлено значение`истинный`, шрифты будут встроены в CSS документа в кодировке Base64.

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


