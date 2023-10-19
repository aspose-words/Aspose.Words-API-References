---
title: HtmlFixedSaveOptions.CssClassNamesPrefix
linktitle: CssClassNamesPrefix
articleTitle: CssClassNamesPrefix
second_title: Aspose.Words for .NET
description: HtmlFixedSaveOptions CssClassNamesPrefix mülk. Style.css dosyasındaki tüm sınıf adlarına eklenen öneki belirtir. Varsayılan değerah  C#'da.
type: docs
weight: 20
url: /tr/net/aspose.words.saving/htmlfixedsaveoptions/cssclassnamesprefix/
---
## HtmlFixedSaveOptions.CssClassNamesPrefix property

Style.css dosyasındaki tüm sınıf adlarına eklenen öneki belirtir. Varsayılan değer:`"ah"` .

```csharp
public string CssClassNamesPrefix { get; set; }
```

## Örnekler

CSS'nin ayrı bir dosyaya nasıl yerleştirileceğini ve tüm CSS sınıfı adlarına nasıl önek ekleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Bookmarks.docx");

HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    CssClassNamesPrefix = "myprefix",
    SaveFontFaceCssSeparately = true
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.AddCssClassNamesPrefix.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.AddCssClassNamesPrefix.html");

Assert.True(Regex.Match(outDocContents,
    "<div class=\"myprefixdiv myprefixpage\" style=\"width:595[.]3pt; height:841[.]9pt;\">" +
    "<div class=\"myprefixdiv\" style=\"left:85[.]05pt; top:36pt; clip:rect[(]0pt,510[.]25pt,74[.]95pt,-85.05pt[)];\">" +
    "<span class=\"myprefixspan myprefixtext001\" style=\"font-size:11pt; left:294[.]73pt; top:0[.]36pt; line-height:12[.]29pt;\">").Success);

outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.AddCssClassNamesPrefix/styles.css");

Assert.True(Regex.Match(outDocContents,
    ".myprefixdiv { position:absolute; } " +
    ".myprefixspan { position:absolute; white-space:pre; color:#000000; font-size:12pt; }").Success);
```

### Ayrıca bakınız

* class [HtmlFixedSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
