---
title: HtmlSaveOptions.HtmlVersion
linktitle: HtmlVersion
articleTitle: HtmlVersion
second_title: Aspose.Words for .NET
description: HtmlSaveOptions HtmlVersion mülk. Belgeyi HTML veya MHTMLye kaydederken kullanılması gereken HTML standardı sürümünü belirtir. Varsayılan değerXhtml  C#'da.
type: docs
weight: 330
url: /tr/net/aspose.words.saving/htmlsaveoptions/htmlversion/
---
## HtmlSaveOptions.HtmlVersion property

Belgeyi HTML veya MHTML'ye kaydederken kullanılması gereken HTML standardı sürümünü belirtir. Varsayılan değer:Xhtml .

```csharp
public HtmlVersion HtmlVersion { get; set; }
```

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

// "ExportXhtmlTransitional" bayrağını "true" olarak ayarlamışsak, belgemiz yalnızca DOCTYPE bildirim başlığını içerecektir.
string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportXhtmlTransitional.html");

if (showDoctypeDeclaration)
    Assert.True(outDocContents.Contains(
        "<?xml version=\"1.0\" encoding=\"utf-8\" standalone=\"no\"?>\r\n" +
        "<!DOCTYPE html PUBLIC \"-//W3C//DTD XHTML 1.0 Transitional//EN\" \"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd\">\r\n" +
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

// HTML belgelerimiz farklı HTML sürümleriyle uyumlu olması açısından ufak farklılıklara sahip olacaktır.
string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.HtmlVersions.html");

switch (htmlVersion)
{
    case HtmlVersion.Html5:
        Assert.True(outDocContents.Contains("<a id=\"_Toc76372689\"></a>"));
        Assert.True(outDocContents.Contains("<a id=\"_Toc76372689\"></a>"));
        Assert.True(outDocContents.Contains("<table style=\"-aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
        break;
    case HtmlVersion.Xhtml:
        Assert.True(outDocContents.Contains("<a name=\"_Toc76372689\"></a>"));
        Assert.True(outDocContents.Contains("<ul type=\"disc\" style=\"margin:0pt; padding-left:0pt\">"));
        Assert.True(outDocContents.Contains("<table cellspacing=\"0\" cellpadding=\"0\" style=\"-aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\""));
        break;
}
```

### Ayrıca bakınız

* enum [HtmlVersion](../../htmlversion/)
* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
