---
title: HtmlSaveOptions.ExportRoundtripInformation
linktitle: ExportRoundtripInformation
articleTitle: ExportRoundtripInformation
second_title: Aspose.Words für .NET
description: Entdecken Sie die ExportRoundtripInformation-Eigenschaft von HtmlSaveOptions zur Steuerung von Roundtrip-Daten in den Formaten HTML, MHTML und EPUB. Optimieren Sie Ihre Exporte noch heute!
type: docs
weight: 240
url: /de/net/aspose.words.saving/htmlsaveoptions/exportroundtripinformation/
---
## HtmlSaveOptions.ExportRoundtripInformation property

Gibt an, ob die Roundtrip-Informationen beim Speichern in HTML, MHTML oder EPUB geschrieben werden sollen. Der Standardwert ist`WAHR` für HTML und`FALSCH` für MHTML und EPUB.

```csharp
public bool ExportRoundtripInformation { get; set; }
```

## Bemerkungen

Das Speichern der Roundtrip-Informationen ermöglicht die Wiederherstellung von Dokumenteigenschaften wie Tabstopps, Kommentare, Kopf- und Fußzeilen beim Laden der HTML-Dokumente in ein[`Document`](../../../aspose.words/document/) Objekt.

Wann`WAHR`, werden die Roundtrip-Informationen als -aw-* CSS-Eigenschaften der entsprechenden HTML-Elemente exportiert.

Wann`FALSCH`, bewirkt, dass keine Roundtrip-Informationen in die erstellten Dateien ausgegeben werden.

## Beispiele

Zeigt, wie versteckte Elemente beim Konvertieren in .html erhalten bleiben.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Beim Konvertieren eines Dokuments in .html werden einige Elemente wie versteckte Lesezeichen, ursprüngliche Formpositionen,
// oder Fußnoten werden entweder entfernt oder in einfachen Text umgewandelt und gehen effektiv verloren.
// Beim Speichern mit einem HtmlSaveOptions-Objekt mit auf „true“ gesetztem ExportRoundtripInformation bleiben diese Elemente erhalten.

// Wenn wir das Dokument als HTML speichern, können wir ein SaveOptions-Objekt übergeben, um zu bestimmen
// wie der Speichervorgang Dokumentelemente exportiert, die HTML nicht unterstützt oder verwendet,
// wie versteckte Lesezeichen und ursprüngliche Formpositionen.
// Wenn wir das Flag „ExportRoundtripInformation“ auf „true“ setzen, bleiben diese Elemente beim Speichervorgang erhalten.
// Wenn wir das Flag „ExportRoundTripInformation“ auf „false“ setzen, werden diese Elemente beim Speichervorgang verworfen.
// Wir möchten solche Elemente beibehalten, wenn wir das gespeicherte HTML mit Aspose.Words laden möchten.
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
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
