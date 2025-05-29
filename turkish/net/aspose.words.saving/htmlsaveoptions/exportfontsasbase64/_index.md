---
title: HtmlSaveOptions.ExportFontsAsBase64
linktitle: ExportFontsAsBase64
articleTitle: ExportFontsAsBase64
second_title: .NET için Aspose.Words
description: HtmlSaveOptions ExportFontsAsBase64 özelliğinin, gelişmiş performans için yazı tiplerini Base64 kodlamasına gömerek HTML'nizi nasıl geliştirdiğini keşfedin. Varsayılan, false.
type: docs
weight: 150
url: /tr/net/aspose.words.saving/htmlsaveoptions/exportfontsasbase64/
---
## HtmlSaveOptions.ExportFontsAsBase64 property

Yazı tipi kaynaklarının HTML'ye Base64 kodlamasıyla gömülmesi gerekip gerekmediğini belirtir. Varsayılan`YANLIŞ` .

```csharp
public bool ExportFontsAsBase64 { get; set; }
```

## Notlar

Varsayılan olarak, yazı tipleri ayrı dosyalara yazılır. Bu seçenek olarak ayarlanırsa`doğru`, yazı tipleri Base64 kodlamasıyla belgenin CSS'sine gömülecek .

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
