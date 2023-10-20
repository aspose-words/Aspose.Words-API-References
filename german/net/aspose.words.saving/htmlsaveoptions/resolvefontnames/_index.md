---
title: HtmlSaveOptions.ResolveFontNames
linktitle: ResolveFontNames
articleTitle: ResolveFontNames
second_title: Aspose.Words für .NET
description: HtmlSaveOptions ResolveFontNames eigendom. Gibt an ob im Dokument verwendete Schriftfamiliennamen gemäß aufgelöst und ersetzt werden.FontSettings beim Schreiben in HTMLbasierte Formate in C#.
type: docs
weight: 410
url: /de/net/aspose.words.saving/htmlsaveoptions/resolvefontnames/
---
## HtmlSaveOptions.ResolveFontNames property

Gibt an, ob im Dokument verwendete Schriftfamiliennamen gemäß aufgelöst und ersetzt werden.[`FontSettings`](../../../aspose.words/document/fontsettings/) beim Schreiben in HTML-basierte Formate.

```csharp
public bool ResolveFontNames { get; set; }
```

## Bemerkungen

Standardmäßig ist diese Option auf eingestellt`FALSCH` und Schriftfamiliennamen werden in Quelldokumenten als angegeben in HTML geschrieben. Das ist,[`FontSettings`](../../../aspose.words/document/fontsettings/) werden ignoriert und es wird keine Auflösung oder Ersetzung von Schriftfamiliennamen durchgeführt.

Wenn diese Option auf eingestellt ist`WAHR` , Aspose.Words verwendet[`FontSettings`](../../../aspose.words/document/fontsettings/) um jeden in einem Quelldokument angegebenen Schriftfamiliennamen in den Namen einer verfügbaren Schriftfamilie aufzulösen und bei Bedarf eine Schriftartenersetzung durchzuführen.

## Beispiele

Zeigt, wie alle Schriftartnamen aufgelöst werden, bevor sie in HTML geschrieben werden.

```csharp
Document doc = new Document(MyDir + "Missing font.docx");

// Dieses Dokument enthält Text, der eine Schriftart benennt, die wir nicht haben.
Assert.NotNull(doc.FontInfos["28 Days Later"]);

// Wenn wir keine Möglichkeit haben, diese Schriftart zu erhalten, aber den gesamten Text anzeigen möchten
// in diesem Dokument in einem Ausgabe-HTML können wir es durch eine andere Schriftart ersetzen.
FontSettings fontSettings = new FontSettings
{
    SubstitutionSettings =
    {
        DefaultFontSubstitution =
        {
            DefaultFontName = "Arial",
            Enabled = true
        }
    }
};

doc.FontSettings = fontSettings;

HtmlSaveOptions saveOptions = new HtmlSaveOptions(SaveFormat.Html)
{
    // Standardmäßig ist diese Option auf „False“ gesetzt und Aspose.Words schreibt Schriftartnamen wie im Quelldokument angegeben
    ResolveFontNames = resolveFontNames
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.ResolveFontNames.html", saveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ResolveFontNames.html");

Assert.True(resolveFontNames
    ? Regex.Match(outDocContents, "<span style=\"font-family:Arial\">").Success
    : Regex.Match(outDocContents, "<span style=\"font-family:\'28 Days Later\'\">").Success);
```

### Siehe auch

* class [HtmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
