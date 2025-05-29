---
title: HtmlFixedSaveOptions.CssClassNamesPrefix
linktitle: CssClassNamesPrefix
articleTitle: CssClassNamesPrefix
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Eigenschaft „HtmlFixedSaveOptions CssClassNamesPrefix“ Ihr Styling verbessert, indem sie allen Klassennamen in Ihrer style.css ein anpassbares Präfix hinzufügt.
type: docs
weight: 20
url: /de/net/aspose.words.saving/htmlfixedsaveoptions/cssclassnamesprefix/
---
## HtmlFixedSaveOptions.CssClassNamesPrefix property

Gibt das Präfix an, das allen Klassennamen in der Datei style.css hinzugefügt wird. Der Standardwert ist`"oh"` .

```csharp
public string CssClassNamesPrefix { get; set; }
```

## Beispiele

Zeigt, wie CSS in eine separate Datei eingefügt und allen CSS-Klassennamen ein Präfix hinzugefügt wird.

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

### Siehe auch

* class [HtmlFixedSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
