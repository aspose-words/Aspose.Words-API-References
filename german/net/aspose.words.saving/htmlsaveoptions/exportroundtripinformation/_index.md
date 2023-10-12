---
title: HtmlSaveOptions.ExportRoundtripInformation
second_title: Aspose.Words für .NET-API-Referenz
description: HtmlSaveOptions eigendom. Gibt an ob die RoundtripInformationen beim Speichern in HTML MHTML oder EPUB geschrieben werden sollen. Der Standardwert istWAHR für HTML undFALSCH für MHTML und EPUB.
type: docs
weight: 240
url: /de/net/aspose.words.saving/htmlsaveoptions/exportroundtripinformation/
---
## HtmlSaveOptions.ExportRoundtripInformation property

Gibt an, ob die Roundtrip-Informationen beim Speichern in HTML, MHTML oder EPUB geschrieben werden sollen. Der Standardwert ist`WAHR` für HTML und`FALSCH` für MHTML und EPUB.

```csharp
public bool ExportRoundtripInformation { get; set; }
```

### Bemerkungen

Durch das Speichern der Roundtrip-Informationen können Dokumenteigenschaften wie Tabstopps, Kommentare, Kopf- und Fußzeilen wiederhergestellt werden, während die HTML-Dokumente wieder in ein geladen werden[`Document`](../../../aspose.words/document/) Objekt.

Wann`WAHR`, werden die Roundtrip-Informationen als -aw-* CSS-Eigenschaften der entsprechenden HTML-Elemente exportiert.

Wann`FALSCH`, bewirkt, dass keine Roundtrip-Informationen in erzeugten Dateien ausgegeben werden.

### Beispiele

Zeigt, wie versteckte Elemente beim Konvertieren in .html erhalten bleiben.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Beim Konvertieren eines Dokuments in .html werden einige Elemente wie versteckte Lesezeichen, ursprüngliche Formpositionen,
// oder Fußnoten werden entweder entfernt oder in einfachen Text umgewandelt und gehen praktisch verloren.
// Beim Speichern mit einem HtmlSaveOptions-Objekt, wobei ExportRoundtripInformation auf true gesetzt ist, bleiben diese Elemente erhalten.

// Wenn wir das Dokument in HTML speichern, können wir zur Bestimmung ein SaveOptions-Objekt übergeben
// wie der Speichervorgang Dokumentelemente exportiert, die HTML nicht unterstützt oder verwendet,
// wie versteckte Lesezeichen und ursprüngliche Formpositionen.
// Wenn wir das Flag „ExportRoundtripInformation“ auf „true“ setzen, bleiben diese Elemente beim Speichervorgang erhalten.
// Wenn wir das Flag „ExportRoundTripInformation“ auf „false“ setzen, verwirft der Speichervorgang diese Elemente.
// Wir möchten solche Elemente beibehalten, wenn wir beabsichtigen, den gespeicherten HTML-Code mit Aspose.Words zu laden.
// da sie noch einmal von Nutzen sein könnten.
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


