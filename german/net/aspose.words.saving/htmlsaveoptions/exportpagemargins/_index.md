---
title: HtmlSaveOptions.ExportPageMargins
linktitle: ExportPageMargins
articleTitle: ExportPageMargins
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Eigenschaft „HtmlSaveOptions ExportPageMargins“ Ihre HTML-, MHTML- und EPUB-Exporte verbessert, indem sie die Seitenränder für eine ansprechende Präsentation steuert.
type: docs
weight: 210
url: /de/net/aspose.words.saving/htmlsaveoptions/exportpagemargins/
---
## HtmlSaveOptions.ExportPageMargins property

Gibt an, ob Seitenränder in HTML, MHTML oder EPUB exportiert werden. Standard ist`FALSCH` .

```csharp
public bool ExportPageMargins { get; set; }
```

## Bemerkungen

Aspose.Words zeigt standardmäßig keinen Bereich der Seitenränder an. Wenn Elemente vollständig oder teilweise durch die Dokumentkante abgeschnitten werden, kann der angezeigte Bereich mit dieser Option erweitert werden.

## Beispiele

Zeigt, wie Objekte außerhalb des zulässigen Bereichs in HTML-Ausgabedokumenten angezeigt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Verwenden Sie einen Builder, um eine Form ohne Umbruch einzufügen.
Shape shape = builder.InsertShape(ShapeType.Cube, 200, 200);

shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.WrapType = WrapType.None;

// Negative Formpositionswerte können dazu führen, dass die Form außerhalb der Seitengrenzen liegt.
// Wenn wir dies in HTML exportieren, wird die Form abgeschnitten angezeigt.
shape.Left = -150;

// Beim Speichern des Dokuments im HTML-Format können wir ein SaveOptions-Objekt übergeben
// um zu entscheiden, ob die Seite angepasst werden soll, um Objekte außerhalb des Rahmens vollständig anzuzeigen.
// Wenn wir das Flag „ExportPageMargins“ auf „true“ setzen, ist die Form im Ausgabe-HTML vollständig sichtbar.
// Wenn wir das Flag "ExportPageMargins" auf "false" setzen,
// Unser Dokument zeigt die abgeschnittene Form an, so wie wir sie in Microsoft Word sehen würden.
HtmlSaveOptions options = new HtmlSaveOptions { ExportPageMargins = exportPageMargins };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportPageMargins.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportPageMargins.html");

if (exportPageMargins)
{
    Assert.True(outDocContents.Contains("<style type=\"text/css\">div.Section_1 { margin:70.85pt }</style>"));
    Assert.True(outDocContents.Contains("<div class=\"Section_1\"><p style=\"margin-top:0pt; margin-left:150pt; margin-bottom:0pt\">"));
}
else
{
    Assert.False(outDocContents.Contains("style type=\"text/css\">"));
    Assert.True(outDocContents.Contains("<div><p style=\"margin-top:0pt; margin-left:220.85pt; margin-bottom:0pt\">"));
}
```

### Siehe auch

* class [HtmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
