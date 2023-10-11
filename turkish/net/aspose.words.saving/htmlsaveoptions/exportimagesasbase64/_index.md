---
title: HtmlSaveOptions.ExportImagesAsBase64
second_title: Aspose.Words for .NET API Referansı
description: HtmlSaveOptions mülk. Görüntülerin HTML MHTML veya EPUB çıkışına Base64 formatında kaydedilip kaydedilmeyeceğini belirtir. VarsayılanYANLIŞ .
type: docs
weight: 170
url: /tr/net/aspose.words.saving/htmlsaveoptions/exportimagesasbase64/
---
## HtmlSaveOptions.ExportImagesAsBase64 property

Görüntülerin HTML, MHTML veya EPUB çıkışına Base64 formatında kaydedilip kaydedilmeyeceğini belirtir. Varsayılan:`YANLIŞ` .

```csharp
public bool ExportImagesAsBase64 { get; set; }
```

### Notlar

Bu özellik olarak ayarlandığında`doğru` görüntü verileri doğrudan x000d_'ye aktarılır **img** öğeler ve ayrı dosyalar oluşturulmaz.

### Örnekler

Kaydedilmiş bir HTML belgesinin içine yazı tiplerinin nasıl yerleştirileceğini gösterir.

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

İçinde gömülü resimler bulunan bir .html belgesinin nasıl kaydedileceğini gösterir.

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

### Ayrıca bakınız

* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../htmlsaveoptions/)
* toplantı [Aspose.Words](../../../)


