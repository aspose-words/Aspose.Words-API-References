---
title: AsposeWordsPrintDocument.CachePrinterSettings
second_title: Aspose.Words for .NET API Reference
description: AsposeWordsPrintDocument method. Reads and caches some fields of PrinterSettings to reduce printing time in C#.
type: docs
weight: 40
url: /net/aspose.words.rendering/asposewordsprintdocument/cacheprintersettings/
---
## AsposeWordsPrintDocument.CachePrinterSettings method

Reads and caches some fields of PrinterSettings to reduce printing time.

```csharp
public void CachePrinterSettings()
```

## Remarks

This method is called before the printing starts if it wasn't executed previously.

## Examples

Shows how to select a page range and a printer to print the document with, and then bring up a print preview.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

PrintPreviewDialog previewDlg = new PrintPreviewDialog();

// Call the "Show" method to get the print preview form to show on top.
previewDlg.Show();

// Initialize the Print Dialog with the number of pages in the document.
PrintDialog printDlg = new PrintDialog();
printDlg.AllowSomePages = true;
printDlg.PrinterSettings.MinimumPage = 1;
printDlg.PrinterSettings.MaximumPage = doc.PageCount;
printDlg.PrinterSettings.FromPage = 1;
printDlg.PrinterSettings.ToPage = doc.PageCount;

if (printDlg.ShowDialog() != DialogResult.OK)
    return;

// Create the "Aspose.Words" implementation of the .NET print document,
// and then pass the printer settings from the dialog.
AsposeWordsPrintDocument awPrintDoc = new AsposeWordsPrintDocument(doc);
awPrintDoc.PrinterSettings = printDlg.PrinterSettings;

// Specify the new color print mode.
awPrintDoc.ColorMode = ColorPrintMode.GrayscaleAuto;

// Use the "CachePrinterSettings" method to reduce time of the first call of the "Print" method.
awPrintDoc.CachePrinterSettings();

// Call the "Hide", and then the "InvalidatePreview" methods to get the print preview to show on top.
previewDlg.Hide();
previewDlg.PrintPreviewControl.InvalidatePreview();

// Pass the "Aspose.Words" print document to the .NET Print Preview dialog.
previewDlg.Document = awPrintDoc;
previewDlg.ShowDialog();

awPrintDoc.Print();            
Console.WriteLine($"The numer of pages printed in color are {awPrintDoc.ColorPagesPrinted}.");
```

### See Also

* class [AsposeWordsPrintDocument](../)
* namespace [Aspose.Words.Rendering](../../asposewordsprintdocument/)
* assembly [Aspose.Words](../../../)
