---
title: HtmlSaveOptions.ExportImagesAsBase64
linktitle: ExportImagesAsBase64
articleTitle: ExportImagesAsBase64
second_title: .NET için Aspose.Words
description: Optimize edilmiş HTML, MHTML veya EPUB çıktısı için görüntüleri Base64 biçiminde kaydetmek üzere HtmlSaveOptions ExportImagesAsBase64 özelliğini keşfedin. Belgenizin kalitesini artırın!
type: docs
weight: 170
url: /tr/net/aspose.words.saving/htmlsaveoptions/exportimagesasbase64/
---
## HtmlSaveOptions.ExportImagesAsBase64 property

Görüntülerin çıktı HTML, MHTML veya EPUB'a Base64 biçiminde kaydedilip kaydedilmeyeceğini belirtir. Varsayılan`YANLIŞ` .

```csharp
public bool ExportImagesAsBase64 { get; set; }
```

## Notlar

Bu özellik şu şekilde ayarlandığında:`doğru` görüntü verileri doğrudan olarak dışa aktarılır**resim** öğeler ve ayrı dosyalar oluşturulmaz.

## Örnekler

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

İçerisinde resimler bulunan bir .html belgesinin nasıl kaydedileceğini gösterir.

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
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
