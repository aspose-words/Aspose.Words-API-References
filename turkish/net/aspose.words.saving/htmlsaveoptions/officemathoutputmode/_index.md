---
title: HtmlSaveOptions.OfficeMathOutputMode
second_title: Aspose.Words for .NET API Referansı
description: HtmlSaveOptions mülk. OfficeMath nesnelerinin HTML MHTML veya EPUBa nasıl aktarılacağını denetler. Varsayılan değerHtmlOfficeMathOutputMode.Image .
type: docs
weight: 400
url: /tr/net/aspose.words.saving/htmlsaveoptions/officemathoutputmode/
---
## HtmlSaveOptions.OfficeMathOutputMode property

OfficeMath nesnelerinin HTML, MHTML veya EPUB'a nasıl aktarılacağını denetler. Varsayılan değer`HtmlOfficeMathOutputMode.Image` .

```csharp
public HtmlOfficeMathOutputMode OfficeMathOutputMode { get; set; }
```

### Örnekler

Microsoft OfficeMath nesnelerinin HTML'ye nasıl dışa aktarılacağının nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

// Belgeyi HTML'ye kaydettiğimizde, SaveOptions nesnesini iletebiliriz
// kaydetme işleminin OfficeMath nesnelerini nasıl işlediğini belirlemek için.
// "OfficeMathOutputMode" özelliğinin "HtmlOfficeMathOutputMode.Image" olarak ayarlanması
// her OfficeMath nesnesini bir görüntüye dönüştürecek.
// "OfficeMathOutputMode" özelliğinin "HtmlOfficeMathOutputMode.MathML" olarak ayarlanması
// her OfficeMath nesnesini MathML'ye dönüştürecek.
// "OfficeMathOutputMode" özelliğinin "HtmlOfficeMathOutputMode.Text" olarak ayarlanması
// her OfficeMath formülünü düz HTML metni kullanarak temsil edecektir.
HtmlSaveOptions options = new HtmlSaveOptions { OfficeMathOutputMode = htmlOfficeMathOutputMode };

doc.Save(ArtifactsDir + "HtmlSaveOptions.OfficeMathOutputMode.html", options);
string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.OfficeMathOutputMode.html");

switch (htmlOfficeMathOutputMode)
{
    case HtmlOfficeMathOutputMode.Image:
        Assert.True(Regex.Match(outDocContents, 
            "<p style=\"margin-top:0pt; margin-bottom:10pt\">" +
                "<img src=\"HtmlSaveOptions.OfficeMathOutputMode.001.png\" width=\"159\" height=\"19\" alt=\"\" style=\"vertical-align:middle; " +
                "-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" +
            "</p>").Success);
        break;
    case HtmlOfficeMathOutputMode.MathML:
        Assert.True(Regex.Match(outDocContents,
            "<p style=\"margin-top:0pt; margin-bottom:10pt; text-align:center\">" +
                "<math xmlns=\"http://www.w3.org/1998/Math/MathML\">" +
                    "<mi>i</mi>" +
                    "<mo>[+]</mo>" +
                    "<mi>b</mi>" +
                    "<mo>-</mo>" +
                    "<mi>c</mi>" +
                    "<mo>≥</mo>" +
                    ".*" +
                "</math>" +
            "</p>").Success);
        break;
    case HtmlOfficeMathOutputMode.Text:
        Assert.True(Regex.Match(outDocContents,
            @"<p style=\""margin-top:0pt; margin-bottom:10pt; text-align:center\"">" +
                @"<span style=\""font-family:'Cambria Math'\"">i[+]b-c≥iM[+]bM-cM </span>" +
            "</p>").Success);
        break;
}
```

### Ayrıca bakınız

* enum [HtmlOfficeMathOutputMode](../../htmlofficemathoutputmode/)
* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../htmlsaveoptions/)
* toplantı [Aspose.Words](../../../)


