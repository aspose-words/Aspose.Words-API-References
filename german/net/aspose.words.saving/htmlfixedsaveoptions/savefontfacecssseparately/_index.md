---
title: HtmlFixedSaveOptions.SaveFontFaceCssSeparately
linktitle: SaveFontFaceCssSeparately
articleTitle: SaveFontFaceCssSeparately
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Eigenschaft SaveFontFaceCssSeparately die CSS-Verwaltung Ihres Dokuments optimiert, indem sie Schriftartregeln für sauberere Exporte in einer separaten Datei speichert.
type: docs
weight: 180
url: /de/net/aspose.words.saving/htmlfixedsaveoptions/savefontfacecssseparately/
---
## HtmlFixedSaveOptions.SaveFontFaceCssSeparately property

Flag gibt an, ob "@font-face" CSS-Regeln in eine separate Datei "fontFaces.css" gespeichert werden sollen, wenn ein Dokument mit externem Stylesheet gespeichert wird (d.h. wenn[`ExportEmbeddedCss`](../exportembeddedcss/) ist`FALSCH` ). Der Standardwert ist`FALSCH` , alle CSS-Regeln werden in eine einzelne Datei „styles.css“ geschrieben.

```csharp
public bool SaveFontFaceCssSeparately { get; set; }
```

## Bemerkungen

Festlegen dieser Eigenschaft auf`WAHR` stellt das alte Verhalten (separate Dateien) wieder her, um die Kompatibilität mit Legacy-Code zu gewährleisten.

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
