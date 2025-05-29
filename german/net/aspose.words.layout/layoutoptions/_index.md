---
title: LayoutOptions Class
linktitle: LayoutOptions
articleTitle: LayoutOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie Aspose.Words.Layout.LayoutOptions, um die Dokumentlayoutsteuerung zu optimieren und Ihr Textverarbeitungserlebnis mit flexiblen Anpassungsoptionen zu verbessern.
type: docs
weight: 3800
url: /de/net/aspose.words.layout/layoutoptions/
---
## LayoutOptions class

Enthält die Optionen zur Steuerung des Dokumentlayoutprozesses.

Um mehr zu erfahren, besuchen Sie die[Konvertieren in das Festseitenformat](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) Dokumentationsartikel.

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
| [Callback](../../aspose.words.layout/layoutoptions/callback/) { get; set; } | Ruft ab oder legt fest[`IPageLayoutCallback`](../ipagelayoutcallback/) Implementierung, die vom Seitenlayoutmodell verwendet wird. |
| [CommentDisplayMode](../../aspose.words.layout/layoutoptions/commentdisplaymode/) { get; set; } | Ruft die Art und Weise ab, wie Kommentare gerendert werden. Der Standardwert istShowInBalloons . |
| [ContinuousSectionPageNumberingRestart](../../aspose.words.layout/layoutoptions/continuoussectionpagenumberingrestart/) { get; set; } | Ruft das Verhalten für die Berechnung der Seitenzahlen ab oder legt es fest, wenn ein fortlaufender Abschnitt die Seitennummerierung neu startet. |
| [IgnorePrinterMetrics](../../aspose.words.layout/layoutoptions/ignoreprintermetrics/) { get; set; } | Ruft ab oder legt fest, ob die Kompatibilitätsoption „Druckermaße zum Layouten von Dokumenten verwenden“ ignoriert wird. Der Standardwert ist`WAHR` . |
| [KeepOriginalFontMetrics](../../aspose.words.layout/layoutoptions/keeporiginalfontmetrics/) { get; set; } | Ruft einen Hinweis ab oder legt ihn fest, ob nach der Schriftartersetzung die ursprünglichen Schriftmetriken verwendet werden sollen. Der Standardwert ist`WAHR` . |
| [RevisionOptions](../../aspose.words.layout/layoutoptions/revisionoptions/) { get; } | Ruft Revisionsoptionen ab. |
| [ShowHiddenText](../../aspose.words.layout/layoutoptions/showhiddentext/) { get; set; } | Ruft ab oder legt fest, ob versteckter Text im Dokument gerendert wird. Der Standardwert ist`FALSCH` . |
| [ShowParagraphMarks](../../aspose.words.layout/layoutoptions/showparagraphmarks/) { get; set; } | Ruft ab oder legt fest, ob Absatzmarken gerendert werden. Der Standardwert ist`FALSCH` . |
| [TextShaperFactory](../../aspose.words.layout/layoutoptions/textshaperfactory/) { get; set; } | Ruft ab oder legt fest[`ITextShaperFactory`](../../aspose.words.shaping/itextshaperfactory/) Implementierung, die für erweiterte Typografie-Rendering-Funktionen verwendet wird. |

## Bemerkungen

Sie erstellen keine Instanzen dieser Klasse direkt. Verwenden Sie die[`LayoutOptions`](../../aspose.words/document/layoutoptions/) -Eigenschaft, um auf die Layoutoptionen dieses Dokuments zuzugreifen.

Beachten Sie, dass nach dem Ändern einer der in dieser Klasse vorhandenen Optionen[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/) Damit die geänderten Optionen auf das Layout angewendet werden, sollte method aufgerufen werden.

## Beispiele

Zeigt, wie Text in einem gerenderten Ausgabedokument ausgeblendet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Versteckten Text einfügen und dann angeben, ob er aus einem gerenderten Dokument weggelassen werden soll.
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
// mit einem Absatzsymbol (¶), wenn wir das Dokument rendern.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

doc.LayoutOptions.ShowParagraphMarks = showParagraphMarks;

doc.Save(ArtifactsDir + "Document.LayoutOptionsParagraphMarks.pdf");
```

Zeigt, wie das Erscheinungsbild von Revisionen in einem gerenderten Ausgabedokument geändert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie eine Revision ein und ändern Sie dann die Farbe aller Revisionen in Grün.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// Entfernen Sie den Balken, der links neben jeder überarbeiteten Zeile erscheint.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;
doc.LayoutOptions.RevisionOptions.RevisionBarsPosition = HorizontalAlignment.Right;

doc.Save(ArtifactsDir + "Revision.LayoutOptionsRevisions.pdf");
```

### Siehe auch

* namensraum [Aspose.Words.Layout](../../aspose.words.layout/)
* Montage [Aspose.Words](../../)
