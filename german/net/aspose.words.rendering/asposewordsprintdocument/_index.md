---
title: AsposeWordsPrintDocument Class
linktitle: AsposeWordsPrintDocument
articleTitle: AsposeWordsPrintDocument
second_title: Aspose.Words für .NET
description: Optimieren Sie den Dokumentendruck mit Aspose.Words.Rendering. Unsere AsposeWordsPrintDocument-Klasse bietet nahtlose Integration für .NET-Anwendungen.
type: docs
weight: 5260
url: /de/net/aspose.words.rendering/asposewordsprintdocument/
---
## AsposeWordsPrintDocument class

Bietet eine Standardimplementierung für den Druck einer[`Document`](../../aspose.words/document/)innerhalb des .NET-Druckframeworks.

Um mehr zu erfahren, besuchen Sie die[Drucken eines Dokuments programmgesteuert oder mithilfe von Dialogen](https://docs.aspose.com/words/net/print-a-document-programmatically-or-using-dialogs/) Dokumentationsartikel.

```csharp
public class AsposeWordsPrintDocument : PrintDocument
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [AsposeWordsPrintDocument](asposewordsprintdocument/)(*[Document](../../aspose.words/document/)*) | Initialisiert eine neue Instanz dieser Klasse. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [ColorMode](../../aspose.words.rendering/asposewordsprintdocument/colormode/) { get; set; } | Ruft ab oder legt fest, wie nicht farbige Seiten gedruckt werden, wenn das Gerät Farbdruck unterstützt. |
| [ColorPagesPrinted](../../aspose.words.rendering/asposewordsprintdocument/colorpagesprinted/) { get; } | Ermittelt die Anzahl der in Farbe gedruckten Seiten (also mitColor auf true gesetzt). |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [CachePrinterSettings](../../aspose.words.rendering/asposewordsprintdocument/cacheprintersettings/)() | Liest und speichert einige Felder vonPrinterSettings um die Druckzeit zu verkürzen. |

## Bemerkungen

`AsposeWordsPrintDocument` ÜberschreibungenPrintEventArgs) , um den in angegebenen Seitenbereich zu druckenPrinterSettings.

Ein einzelnes Word-Dokument kann aus mehreren Abschnitten bestehen, die Seiten mit unterschiedlicher Größe, Ausrichtung und Papierfächern angeben.`AsposeWordsPrintDocument` überschreibt QueryPageSettingsEventArgs) um beim Drucken eines Word-Dokuments Papierformat, Ausrichtung und Papierquelle richtig auszuwählen.

Microsoft Word speichert druckerspezifische Werte für Papierfächer in einem Word-Dokument. Daher wird nur dann aus den richtigen Fächern gedruckt, wenn Sie auf demselben Druckermodell drucken, das bei der Auswahl der Papierfächer ausgewählt wurde. Wenn Sie ein Dokument auf einem anderen Drucker drucken, wird höchstwahrscheinlich das Standardpapierfach verwendet und nicht die im Dokument angegebenen Fächer.

## Beispiele

Zeigt, wie Sie einen Seitenbereich und einen Drucker zum Drucken des Dokuments auswählen und dann eine Druckvorschau aufrufen.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

PrintPreviewDialog previewDlg = new PrintPreviewDialog();

// Rufen Sie die Methode „Show“ auf, um das Druckvorschauformular oben anzuzeigen.
previewDlg.Show();

// Initialisieren Sie den Druckdialog mit der Anzahl der Seiten im Dokument.
PrintDialog printDlg = new PrintDialog();
printDlg.AllowSomePages = true;
printDlg.PrinterSettings.MinimumPage = 1;
printDlg.PrinterSettings.MaximumPage = doc.PageCount;
printDlg.PrinterSettings.FromPage = 1;
printDlg.PrinterSettings.ToPage = doc.PageCount;

if (printDlg.ShowDialog() != DialogResult.OK)
    return;

// Erstellen Sie die "Aspose.Words"-Implementierung des .NET-Druckdokuments,
// und dann die Druckereinstellungen aus dem Dialog übergeben.
AsposeWordsPrintDocument awPrintDoc = new AsposeWordsPrintDocument(doc);
awPrintDoc.PrinterSettings = printDlg.PrinterSettings;

// Geben Sie den neuen Farbdruckmodus an.
awPrintDoc.ColorMode = ColorPrintMode.GrayscaleAuto;

// Verwenden Sie die Methode „CachePrinterSettings“, um die Zeit des ersten Aufrufs der Methode „Print“ zu reduzieren.
awPrintDoc.CachePrinterSettings();

// Rufen Sie die Methoden „Hide“ und dann „InvalidatePreview“ auf, um die Druckvorschau oben anzuzeigen.
previewDlg.Hide();
previewDlg.PrintPreviewControl.InvalidatePreview();

// Übergeben Sie das Druckdokument „Aspose.Words“ an das Dialogfeld „Druckvorschau“ von .NET.
previewDlg.Document = awPrintDoc;
previewDlg.ShowDialog();

awPrintDoc.Print();
Console.WriteLine($"The numer of pages printed in color are {awPrintDoc.ColorPagesPrinted}.");
```

### Siehe auch

* namensraum [Aspose.Words.Rendering](../../aspose.words.rendering/)
* Montage [Aspose.Words](../../)
