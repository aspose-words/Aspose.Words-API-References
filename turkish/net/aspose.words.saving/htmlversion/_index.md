---
title: HtmlVersion Enum
linktitle: HtmlVersion
articleTitle: HtmlVersion
second_title: .NET için Aspose.Words
description: HTML ve MHTML formatlarında belge kaydetmeyi optimize etmek, uyumluluğu ve performansı artırmak için Aspose.Words.Saving.HtmlVersion enum'unu keşfedin.
type: docs
weight: 5870
url: /tr/net/aspose.words.saving/htmlversion/
---
## HtmlVersion enumeration

Belgeyi kaydederken kullanılan HTML sürümünü belirtirHtml ve Mhtml biçimleri.

```csharp
public enum HtmlVersion
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Xhtml | `0` | Belgeyi XHTML 1.0 Geçiş standardına uygun olarak kaydeder. |
| Html5 | `1` | Belgeyi HTML 5 standardına uygun olarak kaydeder. |

## Örnekler

Belgeleri Xhtml 1.0 geçiş standardına dönüştürürken DOCTYPE başlığının nasıl görüntüleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    HtmlVersion = HtmlVersion.Xhtml,
    ExportXhtmlTransitional = showDoctypeDeclaration,
    PrettyFormat = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportXhtmlTransitional.html", options);

// Belgemiz yalnızca "ExportXhtmlTransitional" bayrağını "true" olarak ayarladıysak bir DOCTYPE bildirim başlığı içerecektir.
string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportXhtmlTransitional.html");
string newLine = Environment.NewLine;

if (showDoctypeDeclaration)
    Assert.True(outDocContents.Contains(
        $"<?xml version=\"1.0\" encoding=\"utf-8\" standalone=\"no\"?>{newLine}" +
        $"<!DOCTYPE html PUBLIC \"-//W3C//DTD XHTML 1.0 Geçiş//TR\" \"http://www.w3.org/TR/xhtml1/DTD/xhtml1-geçiş.dtd\">{newLine}" +
        "<html xmlns=\"http://www.w3.org/1999/xhtml\">"));
else
    Assert.True(outDocContents.Contains("<html>"));
```

Bir belgenin belirli bir HTML sürümüne nasıl kaydedileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    HtmlVersion = htmlVersion,
    PrettyFormat = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.HtmlVersions.html", options);

// HTML dokümanlarımız farklı HTML sürümleriyle uyumlu olabilmesi için ufak farklılıklar içerecektir.
string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.HtmlVersions.html");

switch (htmlVersion)
{
    case HtmlVersion.Html5:
        Assert.True(outDocContents.Contains("<a id=\"_Toc76372689\"></a>"));
        Assert.True(outDocContents.Contains("<a id=\"_Toc76372689\"></a>"));
        Assert.True(outDocContents.Contains("<table style=\"padding:0pt; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
        break;
    case HtmlVersion.Xhtml:
        Assert.True(outDocContents.Contains("<a name=\"_Toc76372689\"></a>"));
        Assert.True(outDocContents.Contains("<ul type=\"disc\" style=\"margin:0pt; padding-left:0pt\">"));
        Assert.True(outDocContents.Contains("<table cellspacing=\"0\" cellpadding=\"0\" style=\"-aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\""));
        break;
}
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
