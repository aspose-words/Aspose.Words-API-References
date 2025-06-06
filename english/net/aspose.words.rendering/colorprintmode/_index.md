---
title: ColorPrintMode Enum
linktitle: ColorPrintMode
articleTitle: ColorPrintMode
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Rendering.ColorPrintMode enum for optimized color printing. Control how non-colored pages are printed for enhanced document quality.
type: docs
weight: 5270
url: /net/aspose.words.rendering/colorprintmode/
---
## ColorPrintMode enumeration

Specifies how non-colored pages are printed if the device supports color printing.

```csharp
public enum ColorPrintMode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Normal | `0` | All pages are printed according to the printer's capabilities and settings. |
| GrayscaleAuto | `1` | Non-colored pages if detected are printed in grayscale. |

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

* namespace [Aspose.Words.Rendering](../../aspose.words.rendering/)
* assembly [Aspose.Words](../../)
