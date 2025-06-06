---
title: HtmlSaveOptions.ExportFontsAsBase64
linktitle: ExportFontsAsBase64
articleTitle: ExportFontsAsBase64
second_title: Aspose.Words для .NET
description: Узнайте, как свойство HtmlSaveOptions ExportFontsAsBase64 улучшает ваш HTML, встраивая шрифты в кодировку Base64 для повышения производительности. По умолчанию — false.
type: docs
weight: 150
url: /ru/net/aspose.words.saving/htmlsaveoptions/exportfontsasbase64/
---
## HtmlSaveOptions.ExportFontsAsBase64 property

Указывает, следует ли встраивать ресурсы шрифтов в HTML в кодировке Base64. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool ExportFontsAsBase64 { get; set; }
```

## Примечания

По умолчанию шрифты записываются в отдельные файлы. Если эта опция установлена в`истинный`, шрифты будут встроены в CSS документа в кодировке Base64.

## Примеры

Показывает, как встраивать шрифты в сохраненный HTML-документ.

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
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
