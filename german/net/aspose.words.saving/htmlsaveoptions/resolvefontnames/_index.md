---
title: HtmlSaveOptions.ResolveFontNames
linktitle: ResolveFontNames
articleTitle: ResolveFontNames
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Eigenschaft „HtmlSaveOptions ResolveFontNames“ die Dokumentformatierung verbessert, indem sie genaue Schriftartersetzungen in HTML-Ausgaben gewährleistet.
type: docs
weight: 430
url: /de/net/aspose.words.saving/htmlsaveoptions/resolvefontnames/
---
## HtmlSaveOptions.ResolveFontNames property

Gibt an, ob die im Dokument verwendeten Schriftfamiliennamen aufgelöst und ersetzt werden gemäß [`FontSettings`](../../../aspose.words/document/fontsettings/) beim Schreiben in HTML-basierte Formate.

```csharp
public bool ResolveFontNames { get; set; }
```

## Bemerkungen

Standardmäßig ist diese Option eingestellt auf`FALSCH` und Schriftfamiliennamen werden in HTML als angegeben in Quelldokumenten geschrieben. Das heißt,[`FontSettings`](../../../aspose.words/document/fontsettings/) werden ignoriert und es wird keine Auflösung oder Ersetzung von Schriftfamiliennamen durchgeführt.

Wenn diese Option auf`WAHR` , Aspose.Words verwendet[`FontSettings`](../../../aspose.words/document/fontsettings/) um jeden in einem Quelldokument angegebenen Schriftfamiliennamen in den Namen einer verfügbaren Schriftfamilie aufzulösen und bei Bedarf eine Schriftersetzung durchzuführen.

## Beispiele

Zeigt, wie alle Schriftnamen aufgelöst werden, bevor sie in HTML geschrieben werden.

```csharp
Document doc = new Document(MyDir + "Missing font.docx");

// Dieses Dokument enthält Text, der eine Schriftart benennt, die wir nicht haben.
Assert.NotNull(doc.FontInfos["28 Days Later"]);

// Wenn wir keine Möglichkeit haben, diese Schriftart zu erhalten, und wir den gesamten Text anzeigen möchten
// in diesem Dokument können wir es in einem Ausgabe-HTML durch eine andere Schriftart ersetzen.
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
    // Standardmäßig ist diese Option auf „False“ eingestellt und Aspose.Words schreibt Schriftnamen wie im Quelldokument angegeben
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
