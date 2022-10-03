---
title: ExportRoundtripInformation
second_title: Aspose.Words für .NET-API-Referenz
description: Gibt an ob die RoundtripInformationen beim Speichern in HTML MHTML oder EPUB geschrieben werden. Der Standardwert istStimmt für HTML uFALSCH für MHTML und EPUB.
type: docs
weight: 250
url: /de/net/aspose.words.saving/htmlsaveoptions/exportroundtripinformation/
---
## HtmlSaveOptions.ExportRoundtripInformation property

Gibt an, ob die Roundtrip-Informationen beim Speichern in HTML, MHTML oder EPUB geschrieben werden. Der Standardwert ist`Stimmt` für HTML u`FALSCH` für MHTML und EPUB.

```csharp
public bool ExportRoundtripInformation { get; set; }
```

### Bemerkungen

Das Speichern der Roundtrip-Informationen ermöglicht die Wiederherstellung von Dokumenteigenschaften wie Tabstopps, Kommentaren, Kopf- und Fußzeilen während des Zurückladens von HTML-Dokumenten in ein[`Document`](../../../aspose.words/document/) Objekt.

Wann`Stimmt`, werden die Roundtrip-Informationen als -aw-* CSS properties der entsprechenden HTML-Elemente exportiert.

Wann`FALSCH`bewirkt, dass keine Roundtrip-Informationen in produzierte Dateien ausgegeben werden.

### Beispiele

Zeigt, wie versteckte Elemente beim Konvertieren in .html beibehalten werden.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Beim Konvertieren eines Dokuments in .html werden einige Elemente wie versteckte Lesezeichen, ursprüngliche Formpositionen,
// oder Fußnoten werden entweder entfernt oder in reinen Text umgewandelt und gehen praktisch verloren.
// Beim Speichern mit einem HtmlSaveOptions-Objekt mit ExportRoundtripInformation auf true werden diese Elemente beibehalten.

// Wenn wir das Dokument im HTML-Format speichern, können wir ein SaveOptions-Objekt zur Bestimmung übergeben
// wie der Speichervorgang Dokumentelemente exportiert, die HTML nicht unterstützt oder verwendet,
// wie versteckte Lesezeichen und ursprüngliche Formpositionen.
// Wenn wir das Flag "ExportRoundtripInformation" auf "true" setzen, behält der Speichervorgang diese Elemente bei.
// Wenn wir das Flag "ExportRoundTripInformation" auf "false" setzen, verwirft der Speichervorgang diese Elemente.
// Wir möchten solche Elemente beibehalten, wenn wir beabsichtigen, das gespeicherte HTML mit Aspose.Words zu laden,
// da sie wieder von Nutzen sein könnten.
HtmlSaveOptions options = new HtmlSaveOptions { ExportRoundtripInformation = exportRoundtripInformation };

doc.Save(ArtifactsDir + "HtmlSaveOptions.RoundTripInformation.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.RoundTripInformation.html");
doc = new Document(ArtifactsDir + "HtmlSaveOptions.RoundTripInformation.html");

if (exportRoundtripInformation)
{
    Assert.True(outDocContents.Contains("<div style=\"-aw-headerfooter-type:header-primary; clear:both\">"));
    Assert.True(outDocContents.Contains("<span style=\"-aw-import:ignore\">&#xa0;</span>"));

    Assert.True(outDocContents.Contains(
        "td colspan=\"2\" style=\"width:210.6pt; border-style:solid; border-width:0.75pt 6pt 0.75pt 0.75pt; " +
        "padding-right:2.4pt; padding-left:5.03pt; vertical-align:top; " +
        "-aw-border-bottom:0.5pt single; -aw-border-left:0.5pt single; -aw-border-top:0.5pt single\">"));

    Assert.True(outDocContents.Contains(
        "<li style=\"margin-left:30.2pt; padding-left:5.8pt; -aw-font-family:'Courier New'; -aw-font-weight:normal; -aw-number-format:'o'\">"));

    Assert.True(outDocContents.Contains(
        "<img src=\"HtmlSaveOptions.RoundTripInformation.003.jpeg\" width=\"350\" height=\"180\" alt=\"\" " +
        "style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />"));

    Assert.True(outDocContents.Contains(
        "<span>Page number </span>" +
        "<span style=\"-aw-field-start:true\"></span>" +
        "<span style=\"-aw-field-code:' PAGE   \\\\* MERGEFORMAT '\"></span>" +
        "<span style=\"-aw-field-separator:true\"></span>" +
        "<span>1</span>" +
        "<span style=\"-aw-field-end:true\"></span>"));

    Assert.AreEqual(1, doc.Range.Fields.Count(f => f.Type == FieldType.FieldPage));
}
else
{
    Assert.True(outDocContents.Contains("<div style=\"clear:both\">"));
    Assert.True(outDocContents.Contains("<span>&#xa0;</span>"));

    Assert.True(outDocContents.Contains(
        "<td colspan=\"2\" style=\"width:210.6pt; border-style:solid; border-width:0.75pt 6pt 0.75pt 0.75pt; " +
        "padding-right:2.4pt; padding-left:5.03pt; vertical-align:top\">"));

    Assert.True(outDocContents.Contains(
        "<li style=\"margin-left:30.2pt; padding-left:5.8pt\">"));

    Assert.True(outDocContents.Contains(
        "<img src=\"HtmlSaveOptions.RoundTripInformation.003.jpeg\" width=\"350\" height=\"180\" alt=\"\" />"));

    Assert.True(outDocContents.Contains(
        "<span>Page number 1</span>"));

    Assert.AreEqual(0, doc.Range.Fields.Count(f => f.Type == FieldType.FieldPage));
}
```

### Siehe auch

* class [HtmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../htmlsaveoptions/)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
