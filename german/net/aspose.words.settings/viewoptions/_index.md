---
title: ViewOptions Class
linktitle: ViewOptions
articleTitle: ViewOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Settings.ViewOptions, um die Dokumentanzeige in Microsoft Word anzupassen und so Ihr Bearbeitungserlebnis und Ihre Produktivität zu verbessern.
type: docs
weight: 6780
url: /de/net/aspose.words.settings/viewoptions/
---
## ViewOptions class

Bietet verschiedene Optionen, die steuern, wie ein Dokument in Microsoft Word angezeigt wird.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Optionen und Erscheinungsbild von Word-Dokumenten](https://docs.aspose.com/words/net/work-with-word-document-options-and-appearance/) Dokumentationsartikel.

```csharp
public class ViewOptions
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [DisplayBackgroundShape](../../aspose.words.settings/viewoptions/displaybackgroundshape/) { get; set; } | Steuert die Anzeige der Hintergrundform in der Drucklayoutansicht. |
| [DoNotDisplayPageBoundaries](../../aspose.words.settings/viewoptions/donotdisplaypageboundaries/) { get; set; } | Deaktiviert die Anzeige des Abstands zwischen der Oberkante des Textes und dem oberen Seitenrand. |
| [FormsDesign](../../aspose.words.settings/viewoptions/formsdesign/) { get; set; } | Gibt an, ob sich das Dokument im Formularentwurfsmodus befindet. |
| [ViewType](../../aspose.words.settings/viewoptions/viewtype/) { get; set; } | Steuert den Ansichtsmodus in Microsoft Word. |
| [ZoomPercent](../../aspose.words.settings/viewoptions/zoompercent/) { get; set; } | Ruft den Prozentsatz ab, mit dem Sie Ihr Dokument anzeigen möchten, oder legt diesen fest. |
| [ZoomType](../../aspose.words.settings/viewoptions/zoomtype/) { get; set; } | Ruft einen Zoomwert basierend auf der Fenstergröße ab oder legt ihn fest. |

## Beispiele

Zeigt, wie ein benutzerdefinierter Zoomfaktor festgelegt wird, den ältere Versionen von Microsoft Word beim Laden eines Dokuments anwenden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.ViewOptions.ViewType = ViewType.PageLayout;
doc.ViewOptions.ZoomPercent = 50;

Assert.AreEqual(ZoomType.Custom, doc.ViewOptions.ZoomType);
Assert.AreEqual(ZoomType.None, doc.ViewOptions.ZoomType);

doc.Save(ArtifactsDir + "ViewOptions.SetZoomPercentage.doc");
```

Zeigt, wie ein benutzerdefinierter Zoomtyp festgelegt wird, den ältere Versionen von Microsoft Word beim Laden auf ein Dokument anwenden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Setzen Sie die Eigenschaft „ZoomType“ auf „ZoomType.PageWidth“, um Microsoft Word zu erhalten
// um das Dokument automatisch auf die Seitenbreite zu zoomen.
// Setzen Sie die Eigenschaft „ZoomType“ auf „ZoomType.FullPage“, um Microsoft Word zu erhalten
// um das Dokument automatisch zu vergrößern und die gesamte erste Seite sichtbar zu machen.
// Setzen Sie die Eigenschaft „ZoomType“ auf „ZoomType.TextFit“, um Microsoft Word zu erhalten
// um das Dokument automatisch so zu vergrößern, dass es an die inneren Textränder der ersten Seite angepasst ist.
doc.ViewOptions.ZoomType = zoomType;

doc.Save(ArtifactsDir + "ViewOptions.SetZoomType.doc");
```

### Siehe auch

* class [Document](../../aspose.words/document/)
* property [ViewOptions](../../aspose.words/document/viewoptions/)
* namensraum [Aspose.Words.Settings](../../aspose.words.settings/)
* Montage [Aspose.Words](../../)
