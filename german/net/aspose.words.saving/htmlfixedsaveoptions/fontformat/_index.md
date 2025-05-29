---
title: HtmlFixedSaveOptions.FontFormat
linktitle: FontFormat
articleTitle: FontFormat
second_title: Aspose.Words für .NET
description: Entdecken Sie die FontFormat-Eigenschaft von HtmlFixedSaveOptions, um den Schriftartenexport anzupassen. Stellen Sie Ihr Standardformat einfach auf Woff ein und optimieren Sie es für eine bessere Leistung.
type: docs
weight: 90
url: /de/net/aspose.words.saving/htmlfixedsaveoptions/fontformat/
---
## HtmlFixedSaveOptions.FontFormat property

Ruft ab oder legt fest[`ExportFontFormat`](../../exportfontformat/) Wird für den Schriftartenexport verwendet. Der Standardwert istWoff .

```csharp
public ExportFontFormat FontFormat { get; set; }
```

## Beispiele

Zeigt, wie beim Speichern eines Dokuments im HTML-Format nur Schriftarten vom Zielcomputer verwendet werden.

```csharp
Document doc = new Document(MyDir + "Bullet points with alternative font.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions
{
    ExportEmbeddedCss = true,
    UseTargetMachineFonts = useTargetMachineFonts,
    FontFormat = ExportFontFormat.Ttf,
    ExportEmbeddedFonts = false,
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.UsingMachineFonts.html");

if (useTargetMachineFonts)
    Assert.False(Regex.Match(outDocContents, "@font-face").Success);
else
    Assert.True(Regex.Match(outDocContents,
        "@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], " +
        "url[(]'HtmlFixedSaveOptions.UsingMachineFonts/font001.ttf'[)] format[(]'truetype'[)]; }").Success);
```

### Siehe auch

* enum [ExportFontFormat](../../exportfontformat/)
* class [HtmlFixedSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
