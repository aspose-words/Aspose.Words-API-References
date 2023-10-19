---
title: HtmlOfficeMathOutputMode Enum
linktitle: HtmlOfficeMathOutputMode
articleTitle: HtmlOfficeMathOutputMode
second_title: Aspose.Words for .NET
description: Aspose.Words.Saving.HtmlOfficeMathOutputMode Sıralama. Aspose.Wordsün OfficeMathi HTML MHTML ve EPUBa nasıl aktardığını belirtir C#'da.
type: docs
weight: 5100
url: /tr/net/aspose.words.saving/htmlofficemathoutputmode/
---
## HtmlOfficeMathOutputMode enumeration

Aspose.Words'ün OfficeMath'i HTML, MHTML ve EPUB'a nasıl aktardığını belirtir.

```csharp
public enum HtmlOfficeMathOutputMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Image | `0` | OfficeMath, &lt;img&gt; etiketiyle belirtilen resim olarak HTML'ye dönüştürülür. |
| MathML | `1` | OfficeMath, MathML. kullanılarak HTML'ye dönüştürülür |
| Text | `2` | OfficeMath, &lt;span&gt; etiketleri tarafından belirtilen çalıştırma sırası olarak HTML'ye dönüştürülür. |

## Örnekler

Microsoft OfficeMath nesnelerinin HTML'ye nasıl aktarılacağının nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

// Belgeyi HTML'ye kaydettiğimizde SaveOptions nesnesini iletebiliriz
// kaydetme işleminin OfficeMath nesnelerini nasıl işleyeceğini belirlemek için.
// "OfficeMathOutputMode" özelliğinin "HtmlOfficeMathOutputMode.Image" olarak ayarlanması
// her OfficeMath nesnesini bir görüntüye dönüştürecek.
// "OfficeMathOutputMode" özelliğinin "HtmlOfficeMathOutputMode.MathML" olarak ayarlanması
// her OfficeMath nesnesini MathML'ye dönüştürecek.
// "OfficeMathOutputMode" özelliğinin "HtmlOfficeMathOutputMode.Text" olarak ayarlanması
// her OfficeMath formülünü düz HTML metni kullanarak temsil edecek.
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

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
