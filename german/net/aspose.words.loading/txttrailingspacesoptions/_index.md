---
title: TxtTrailingSpacesOptions Enum
linktitle: TxtTrailingSpacesOptions
articleTitle: TxtTrailingSpacesOptions
second_title: Aspose.Words für .NET
description: Aspose.Words.Loading.TxtTrailingSpacesOptions opsomming. Gibt die verfügbaren Optionen für die Behandlung von nachgestellten Leerzeichen beim Import aus anText Datei in C#.
type: docs
weight: 3740
url: /de/net/aspose.words.loading/txttrailingspacesoptions/
---
## TxtTrailingSpacesOptions enumeration

Gibt die verfügbaren Optionen für die Behandlung von nachgestellten Leerzeichen beim Import aus anText Datei.

```csharp
public enum TxtTrailingSpacesOptions
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Trim | `0` |  |
| Preserve | `1` |  |

## Beispiele

Zeigt, wie Leerzeichen beim Laden von Klartextdokumenten entfernt werden.

```csharp
string textDoc = "      Line 1 \n" +
                 "    Line 2   \n" +
                 " Line 3       ";

// Erstelle ein „TxtLoadOptions“-Objekt, das wir an den Konstruktor eines Dokuments übergeben können
// um zu ändern, wie wir ein Klartextdokument laden.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// Setzen Sie die Eigenschaft „LeadingSpacesOptions“ auf „TxtLeadingSpacesOptions.Preserve“
// um alle Leerzeichen am Anfang jeder Zeile beizubehalten.
// Setzen Sie die Eigenschaft „LeadingSpacesOptions“ auf „TxtLeadingSpacesOptions.ConvertToIndent“
// um alle Leerzeichen am Anfang jeder Zeile zu entfernen,
// und wenden Sie dann einen linken Einzug in der ersten Zeile auf den Absatz an, um die Wirkung der Leerzeichen zu simulieren.
// Setzen Sie die Eigenschaft „LeadingSpacesOptions“ auf „TxtLeadingSpacesOptions.Trim“
// um alle Leerzeichen am Anfang jeder Zeile zu entfernen.
loadOptions.LeadingSpacesOptions = txtLeadingSpacesOptions;

// Setzen Sie die Eigenschaft „TrailingSpacesOptions“ auf „TxtTrailingSpacesOptions.Preserve“
 // um alle Leerzeichen am Ende jeder Zeile beizubehalten.
 // Die Eigenschaft „TrailingSpacesOptions“ auf „TxtTrailingSpacesOptions.Trim“ setzen
// alle Leerzeichen vom Ende jeder Zeile entfernen.
loadOptions.TrailingSpacesOptions = txtTrailingSpacesOptions;

Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(textDoc)), loadOptions);
ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

switch (txtLeadingSpacesOptions)
{
    case TxtLeadingSpacesOptions.ConvertToIndent:
        Assert.AreEqual(37.8d, paragraphs[0].ParagraphFormat.FirstLineIndent);
        Assert.AreEqual(25.2d, paragraphs[1].ParagraphFormat.FirstLineIndent);
        Assert.AreEqual(6.3d, paragraphs[2].ParagraphFormat.FirstLineIndent);

        Assert.True(paragraphs[0].GetText().StartsWith("Line 1"));
        Assert.True(paragraphs[1].GetText().StartsWith("Line 2"));
        Assert.True(paragraphs[2].GetText().StartsWith("Line 3"));
        break;
    case TxtLeadingSpacesOptions.Preserve:
        Assert.True(paragraphs.All(p => ((Paragraph)p).ParagraphFormat.FirstLineIndent == 0.0d));

        Assert.True(paragraphs[0].GetText().StartsWith("      Line 1"));
        Assert.True(paragraphs[1].GetText().StartsWith("    Line 2"));
        Assert.True(paragraphs[2].GetText().StartsWith(" Line 3"));
        break;
    case TxtLeadingSpacesOptions.Trim:
        Assert.True(paragraphs.All(p => ((Paragraph)p).ParagraphFormat.FirstLineIndent == 0.0d));

        Assert.True(paragraphs[0].GetText().StartsWith("Line 1"));
        Assert.True(paragraphs[1].GetText().StartsWith("Line 2"));
        Assert.True(paragraphs[2].GetText().StartsWith("Line 3"));
        break;
}

switch (txtTrailingSpacesOptions)
{
    case TxtTrailingSpacesOptions.Preserve:
        Assert.True(paragraphs[0].GetText().EndsWith("Line 1 \r"));
        Assert.True(paragraphs[1].GetText().EndsWith("Line 2   \r"));
        Assert.True(paragraphs[2].GetText().EndsWith("Line 3       \f"));
        break;
    case TxtTrailingSpacesOptions.Trim:
        Assert.True(paragraphs[0].GetText().EndsWith("Line 1\r"));
        Assert.True(paragraphs[1].GetText().EndsWith("Line 2\r"));
        Assert.True(paragraphs[2].GetText().EndsWith("Line 3\f"));
        break;
}
```

### Siehe auch

* namensraum [Aspose.Words.Loading](../../aspose.words.loading/)
* Montage [Aspose.Words](../../)
