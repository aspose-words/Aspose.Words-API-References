---
title: HtmlSaveOptions.ExportPageMargins
second_title: Aspose.Words für .NET-API-Referenz
description: HtmlSaveOptions eigendom. Gibt an ob Seitenränder in HTML MHTML oder EPUB exportiert werden. Standard istFALSCH .
type: docs
weight: 220
url: /de/net/aspose.words.saving/htmlsaveoptions/exportpagemargins/
---
## HtmlSaveOptions.ExportPageMargins property

Gibt an, ob Seitenränder in HTML, MHTML oder EPUB exportiert werden. Standard ist`FALSCH` .

```csharp
public bool ExportPageMargins { get; set; }
```

### Bemerkungen

Aspose.Words zeigt standardmäßig keinen Bereich der Seitenränder an. Wenn Elemente ganz oder teilweise vom Dokumentrand abgeschnitten werden, kann der angezeigte Bereich mit dieser Option erweitert werden.

### Beispiele

Zeigt, wie Out-of-Bounds-Objekte in Ausgabe-HTML-Dokumenten angezeigt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Verwenden Sie einen Builder, um eine Form ohne Umbruch einzufügen.
Shape shape = builder.InsertShape(ShapeType.Cube, 200, 200);

shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.WrapType = WrapType.None;

// Negative Formpositionswerte können die Form außerhalb der Seitengrenzen platzieren.
// Wenn wir dies nach HTML exportieren, wird die Form abgeschnitten angezeigt.
shape.Left = -150;

// Beim Speichern des Dokuments im HTML-Format können wir ein SaveOptions-Objekt übergeben
// um zu entscheiden, ob die Seite angepasst werden soll, um Out-of-Bounds-Objekte vollständig anzuzeigen.
// Wenn wir das Flag "ExportPageMargins" auf "true" setzen, wird die Form im Ausgabe-HTML vollständig sichtbar sein.
// Wenn wir das Flag "ExportPageMargins" auf "false" setzen,
// Unser Dokument zeigt die Form abgeschnitten an, wie wir es in Microsoft Word sehen würden.
HtmlSaveOptions options = new HtmlSaveOptions { ExportPageMargins = exportPageMargins };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportPageMargins.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportPageMargins.html");

if (exportPageMargins)
{
    Assert.True(outDocContents.Contains("<style type=\"text/css\">div.Section1 { margin:70.85pt }</style>"));
    Assert.True(outDocContents.Contains("<div class=\"Section1\"><p style=\"margin-top:0pt; margin-left:151pt; margin-bottom:0pt\">"));
}
else
{
    Assert.False(outDocContents.Contains("style type=\"text/css\">"));
    Assert.True(outDocContents.Contains("<div><p style=\"margin-top:0pt; margin-left:221.85pt; margin-bottom:0pt\">"));
}
```

### Siehe auch

* class [HtmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../htmlsaveoptions/)
* Montage [Aspose.Words](../../../)


