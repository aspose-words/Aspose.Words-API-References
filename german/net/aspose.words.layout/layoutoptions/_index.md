---
title: Class LayoutOptions
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Layout.LayoutOptions klas. Enthält die Optionen die die Steuerung des Dokumentlayoutprozesses ermöglichen.
type: docs
weight: 3350
url: /de/net/aspose.words.layout/layoutoptions/
---
## LayoutOptions class

Enthält die Optionen, die die Steuerung des Dokumentlayoutprozesses ermöglichen.

Um mehr zu erfahren, besuchen Sie die[Konvertieren in das Fixed-Page-Format](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) Dokumentationsartikel.

```csharp
public class LayoutOptions
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [LayoutOptions](layoutoptions/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Callback](../../aspose.words.layout/layoutoptions/callback/) { get; set; } | Ruft ab oder legt fest[`IPageLayoutCallback`](../ipagelayoutcallback/) Vom Seitenlayoutmodell verwendete Implementierung. |
| [CommentDisplayMode](../../aspose.words.layout/layoutoptions/commentdisplaymode/) { get; set; } | Ruft ab oder legt fest, wie Kommentare gerendert werden. Der Standardwert istShowInBalloons . |
| [ContinuousSectionPageNumberingRestart](../../aspose.words.layout/layoutoptions/continuoussectionpagenumberingrestart/) { get; set; } | Ruft den Verhaltensmodus für die Berechnung von Seitenzahlen ab oder legt diesen fest, wenn ein fortlaufender Abschnitt die Seitennummerierung neu startet. |
| [IgnorePrinterMetrics](../../aspose.words.layout/layoutoptions/ignoreprintermetrics/) { get; set; } | Ruft die Angabe ab, ob die Kompatibilitätsoption „Druckermetriken zum Layouten des Dokuments verwenden“ ignoriert wird, oder legt diese fest. Standard ist`WAHR` . |
| [KeepOriginalFontMetrics](../../aspose.words.layout/layoutoptions/keeporiginalfontmetrics/) { get; set; } | Ruft einen Hinweis ab, ob die ursprünglichen Schriftartmetriken nach der Schriftartersetzung verwendet werden sollen, oder legt diesen fest. Der Standardwert ist`WAHR` . |
| [RevisionOptions](../../aspose.words.layout/layoutoptions/revisionoptions/) { get; } | Ruft Revisionsoptionen ab. |
| [ShowHiddenText](../../aspose.words.layout/layoutoptions/showhiddentext/) { get; set; } | Ruft den Hinweis ab, ob versteckter Text im Dokument gerendert wird, oder legt diesen fest. Standard ist`FALSCH` . |
| [ShowParagraphMarks](../../aspose.words.layout/layoutoptions/showparagraphmarks/) { get; set; } | Ruft den Hinweis ab, ob Absatzmarken gerendert werden, oder legt diesen fest. Der Standardwert ist`FALSCH` . |
| [TextShaperFactory](../../aspose.words.layout/layoutoptions/textshaperfactory/) { get; set; } | Ruft ab oder legt fest[`ITextShaperFactory`](../../aspose.words.shaping/itextshaperfactory/) Implementierung, die für erweiterte Typografie-Renderingfunktionen verwendet wird. |

### Bemerkungen

Sie erstellen keine Instanzen dieser Klasse direkt. Benutzen Sie die[`LayoutOptions`](../../aspose.words/document/layoutoptions/) Eigenschaft, um auf Layoutoptionen für dieses Dokument zuzugreifen.

Beachten Sie, dass nach dem Ändern einer der in dieser Klasse vorhandenen Optionen[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/) method sollte aufgerufen werden, damit die geänderten Optionen auf das Layout angewendet werden.

### Beispiele

Zeigt, wie Text in einem gerenderten Ausgabedokument ausgeblendet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Versteckten Text einfügen und dann angeben, ob wir ihn in einem gerenderten Dokument weglassen möchten.
builder.Writeln("This text is not hidden.");
builder.Font.Hidden = true;
builder.Writeln("This text is hidden.");

doc.LayoutOptions.ShowHiddenText = showHiddenText;

doc.Save(ArtifactsDir + "Document.LayoutOptionsHiddenText.pdf");
```

Zeigt, wie Absatzmarken in einem gerenderten Ausgabedokument angezeigt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Fügen Sie einige Absätze hinzu und aktivieren Sie dann Absatzmarken, um die Enden der Absätze anzuzeigen
// mit einem Pilcrow-Symbol (¶), wenn wir das Dokument rendern.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

doc.LayoutOptions.ShowParagraphMarks = showParagraphMarks;

doc.Save(ArtifactsDir + "Document.LayoutOptionsParagraphMarks.pdf");
```

Zeigt, wie das Erscheinungsbild von Revisionen in einem gerenderten Ausgabedokument geändert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Eine Revision einfügen und dann die Farbe aller Revisionen in Grün ändern.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// Entfernen Sie die Leiste, die links von jeder überarbeiteten Zeile erscheint.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;

doc.Save(ArtifactsDir + "Document.LayoutOptionsRevisions.pdf");
```

### Siehe auch

* namensraum [Aspose.Words.Layout](../../aspose.words.layout/)
* Montage [Aspose.Words](../../)


