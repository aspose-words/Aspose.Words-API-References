---
title: AsposeWordsPrintDocument.ColorMode
linktitle: ColorMode
articleTitle: ColorMode
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie den Druck mit der ColorMode-Eigenschaft von AsposeWordsPrintDocument optimieren. Steuern Sie die nicht-farbige Seitenausgabe für verbesserten Farbdruck!
type: docs
weight: 20
url: /de/net/aspose.words.rendering/asposewordsprintdocument/colormode/
---
## AsposeWordsPrintDocument.ColorMode property

Ruft ab oder legt fest, wie nicht farbige Seiten gedruckt werden, wenn das Gerät Farbdruck unterstützt.

```csharp
public ColorPrintMode ColorMode { get; set; }
```

## Bemerkungen

Hat keinen Einfluss auf den Broschürendruck.

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

* enum [ColorPrintMode](../../colorprintmode/)
* class [AsposeWordsPrintDocument](../)
* namensraum [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* Montage [Aspose.Words](../../../)
