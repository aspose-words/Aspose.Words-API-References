---
title: Enum HtmlVersion
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Saving.HtmlVersion Sıralama. Belgeyi şuraya kaydederken HTML sürümünün kullanıldığını gösterir.Html ve Mhtml biçimler.
type: docs
weight: 4860
url: /tr/net/aspose.words.saving/htmlversion/
---
## HtmlVersion enumeration

Belgeyi şuraya kaydederken HTML sürümünün kullanıldığını gösterir.Html ve Mhtml biçimler.

```csharp
public enum HtmlVersion
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Xhtml | `0` | Belgeyi XHTML 1.0 Geçiş standardına uygun olarak kaydeder. |
| Html5 | `1` | Belgeyi HTML 5 standardına uygun olarak kaydeder. |

### Örnekler

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

// "ExportXhtmlTransitional" bayrağını "true" olarak ayarlamışsak, belgemiz yalnızca bir DOCTYPE bildirim başlığı içerecektir.
string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportXhtmlTransitional.html");

if (showDoctypeDeclaration)
    Assert.True(outDocContents.Contains(
        "<?xml version=\"1.0\" encoding=\"utf-8\" standalone=\"no\"?>\r\n" +
        "<!DOCTYPE html PUBLIC \"-//W3C//DTD XHTML 1.0 Transitional//EN\" \"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd\">\r\n" +
        "<html xmlns=\"http://www.w3.org/1999/xhtml\">");
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

// HTML belgelerimiz, farklı HTML sürümleriyle uyumlu olması için küçük farklılıklara sahip olacaktır.
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

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)


