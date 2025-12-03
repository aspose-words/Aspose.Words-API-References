---
title: AsposeWordsPrintDocument Class
linktitle: AsposeWordsPrintDocument
articleTitle: AsposeWordsPrintDocument
second_title: Aspose.Words for .NET
description: Streamline document printing with Aspose.Words.Rendering. Our AsposeWordsPrintDocument class offers seamless integration for .NET applications.
type: docs
weight: 5300
url: /net/aspose.words.rendering/asposewordsprintdocument/
---
## AsposeWordsPrintDocument class

Provides a default implementation for printing of a [`Document`](../../aspose.words/document/) within the .NET printing framework.

To learn more, visit the [Printing a Document Programmatically or Using Dialogs](https://docs.aspose.com/words/net/print-a-document-programmatically-or-using-dialogs/) documentation article.

```csharp
public class AsposeWordsPrintDocument : PrintDocument
```

## Constructors

| Name | Description |
| --- | --- |
| [AsposeWordsPrintDocument](asposewordsprintdocument/)(*[Document](../../aspose.words/document/)*) | Initializes a new instance of this class. |

## Properties

| Name | Description |
| --- | --- |
| [ColorMode](../../aspose.words.rendering/asposewordsprintdocument/colormode/) { get; set; } | Gets or sets how non-colored pages are printed if the device supports color printing. |
| [ColorPagesPrinted](../../aspose.words.rendering/asposewordsprintdocument/colorpagesprinted/) { get; } | Gets the number of pages printed in color (i.e. with Color set to true). |
| [PageIndexFilter](../../aspose.words.rendering/asposewordsprintdocument/pageindexfilter/) { get; set; } | Gets or sets the zero-based index filter used to determine which pages to skip during printing. |
| [PagesRemaining](../../aspose.words.rendering/asposewordsprintdocument/pagesremaining/) { get; } | Gets the number of pages remaining in the currently active print job. |
| [TotalPagesPrinted](../../aspose.words.rendering/asposewordsprintdocument/totalpagesprinted/) { get; } | Gets the total number of pages actually printed during the print session. |

## Methods

| Name | Description |
| --- | --- |
| [CachePrinterSettings](../../aspose.words.rendering/asposewordsprintdocument/cacheprintersettings/)() | Reads and caches some fields of PrinterSettings to reduce printing time. |

## Remarks

`AsposeWordsPrintDocument` overrides PrintEventArgs) to print the range of pages that is specified in PrinterSettings.

A single Word document can consist of multiple sections that specify pages with different sizes, orientation and paper trays. `AsposeWordsPrintDocument` overrides QueryPageSettingsEventArgs) to properly select paper size, orientation and paper source when printing a Word document.

Microsoft Word stores printer specific values for paper trays in a Word document and therefore, only printing on the same printer model as the one that was selected when the user specified the paper trays will result in printing from the correct trays. If you print a document on a different printer, then most likely the default paper tray will be used, not the trays specified in the document.

## Examples

Shows how to monitor printing progress.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Initialize the printer settings.
PrinterSettings printerSettings = new PrinterSettings();
printerSettings.PrinterName = "Microsoft Print to PDF";
printerSettings.PrintRange = PrintRange.AllPages;

// Create a special Aspose.Words implementation of the .NET PrintDocument class.
// Pass the printer settings from the print dialog to the print document.
AsposeWordsPrintDocument printDoc = new AsposeWordsPrintDocument(doc);
printDoc.PrinterSettings = printerSettings;

// Initialize the custom printing tracker.
PrintTracker printTracker = new PrintTracker(printDoc);

printDoc.Print();

// Write the event log.
foreach (string eventString in printTracker.EventLog)
    Console.WriteLine(eventString);
```

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
Console.WriteLine($"The number of pages printed in color are {awPrintDoc.ColorPagesPrinted}.");
```

Shows an example class for monitoring the progress of printing.

```csharp
/// <summary>
    /// Tracks printing progress of an Aspose.Words document and logs printing events.
    /// </summary>
    internal class PrintTracker
    {
        /// <summary>
        /// Initializes a new instance of the SamplePrintTracker class
        /// and subscribes to printing events of the specified document.
        /// </summary>
        /// <param name="printDoc">The Aspose.Words print document to track.</param>
        /// <exception cref="ArgumentNullException">Thrown when <paramref name="printDoc"/> is null.</exception>
        internal PrintTracker(AsposeWordsPrintDocument printDoc)
        {
            if (printDoc == null)
                throw new ArgumentNullException(nameof(printDoc));

            printDoc.BeginPrint += PrintDocument_BeginPrint;
            printDoc.EndPrint += PrintDocument_EndPrint;
            printDoc.PrintPage += PrintDocument_PrintPage;
        }

        /// <summary>
        /// Gets the current page being printed (1-based index).
        /// Returns -1 when no printing is in progress.
        /// </summary>
        internal int PrintingPage { get; private set; } = -1;

        /// <summary>
        /// Gets the total number of pages to print.
        /// Returns 0 when no printing is in progress.
        /// </summary>
        internal int TotalPages { get; private set; }

        /// <summary>
        /// Gets the log of printing events in chronological order.
        /// </summary>
        internal IReadOnlyList<string> EventLog { get; } = new List<string>();

        private void PrintDocument_BeginPrint(object sender, PrintEventArgs e)
        {
            var printDoc = (AsposeWordsPrintDocument)sender;

            PrintingPage = -1;
            TotalPages = printDoc.PagesRemaining;

            AddLogEntry($"BeginPrint. {printDoc.PagesRemaining} pages left to print.");
        }

        private void PrintDocument_PrintPage(object sender, PrintPageEventArgs e)
        {
            var printDoc = (AsposeWordsPrintDocument)sender;

            PrintingPage = TotalPages - printDoc.PagesRemaining + 1;

            AddLogEntry($"Printing page {PrintingPage} of {TotalPages}");
        }

        private void PrintDocument_EndPrint(object sender, PrintEventArgs e)
        {
            var printDoc = (AsposeWordsPrintDocument)sender;

            PrintingPage = -1;
            TotalPages = 0;

            AddLogEntry($"EndPrint. {printDoc.PagesRemaining} pages left to print.");
        }

        private void AddLogEntry(string message)
        {
            ((List<string>)EventLog).Add(message);
        }
    }
}
```

### See Also

* namespace [Aspose.Words.Rendering](../../aspose.words.rendering/)
* assembly [Aspose.Words](../../)
