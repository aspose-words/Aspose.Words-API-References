---
title: HtmlSaveOptions.ExportShapesAsSvg
second_title: Aspose.Words für .NET-API-Referenz
description: HtmlSaveOptions eigendom. Steuert obShape Knoten werden beim Speichern in HTML MHTML oder EPUB in SVGBilder konvertiert. Standardwert istFALSCH .
type: docs
weight: 260
url: /de/net/aspose.words.saving/htmlsaveoptions/exportshapesassvg/
---
## HtmlSaveOptions.ExportShapesAsSvg property

Steuert ob[`Shape`](../../../aspose.words.drawing/shape/) Knoten werden beim Speichern in HTML, MHTML oder EPUB in SVG-Bilder konvertiert. Standardwert ist`FALSCH` .

```csharp
public bool ExportShapesAsSvg { get; set; }
```

### Bemerkungen

Wenn diese Option auf gesetzt ist`Stimmt` ,[`Shape`](../../../aspose.words.drawing/shape/) Knoten werden als &lt;svg&gt;-Elemente exportiert. Andernfalls werden sie in Bitmaps gerendert und als &lt;img&gt;-Elemente exportiert.

Beachten Sie, dass sich diese Optionen auch auf Textfelder auswirken, da sie durch dargestellt werden[`Shape`](../../../aspose.words.drawing/shape/) nodes. Als Ergebnis, wenn diese Option auf gesetzt ist`Stimmt` , es überschreibt dieExportTextBoxAsSvgEigenschaft Wert und bewirkt, dass Textfelder in SVG. konvertiert werden

### Beispiele

Zeigt, wie Formen als skalierbare Vektorgrafiken exportiert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBox = builder.InsertShape(ShapeType.TextBox, 100.0, 60.0);
builder.MoveTo(textBox.FirstParagraph);
builder.Write("My text box");

// Wenn wir das Dokument im HTML-Format speichern, können wir ein SaveOptions-Objekt übergeben
// um zu bestimmen, wie der Speichervorgang Textfeldformen exportiert.
// Wenn wir das Flag "ExportTextBoxAsSvg" auf "true" setzen,
// Die Speicheroperation konvertiert Formen mit Text in SVG-Objekte.
// Wenn wir das Flag "ExportTextBoxAsSvg" auf "false" setzen,
// Die Speicheroperation wandelt Formen mit Text in Bilder um.
HtmlSaveOptions options = new HtmlSaveOptions { ExportShapesAsSvg = exportShapesAsSvg };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportTextBox.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportTextBox.html");

if (exportShapesAsSvg)
{
    Assert.True(outDocContents.Contains(
        "<span style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\">" +
        "<svg xmlns=\"http://www.w3.org/2000/svg\" xmlns:xlink=\"http://www.w3.org/1999/xlink\" version=\"1.1\" width=\"133\" height= \"80\">"));
}
else
{
    Assert.True(outDocContents.Contains(
        "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
            "<img src=\"HtmlSaveOptions.ExportTextBox.001.png\" width=\"136\" height=\"83\" alt=\"\" " +
            "style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" +
        "</p>"));
}
```

### Siehe auch

* class [HtmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../htmlsaveoptions/)
* Montage [Aspose.Words](../../../)


