---
title: AsposeWordsPrintDocument.PagesRemaining
linktitle: PagesRemaining
articleTitle: PagesRemaining
second_title: Aspose.Words for .NET
description: Track remaining pages in active print jobs with AsposeWordsPrintDocument PagesRemaining property for print control.
type: docs
weight: 40
url: /net/aspose.words.rendering/asposewordsprintdocument/pagesremaining/
---
## AsposeWordsPrintDocument.PagesRemaining property

Gets the number of pages remaining in the currently active print job.

```csharp
public int PagesRemaining { get; }
```

## Remarks

This value is updated automatically as pages are printed, reflecting the current print job's progress. Outside of print time and in case of print job errors or interruptions, the value may not reflect the actual number of pages pending.

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

* class [AsposeWordsPrintDocument](../)
* namespace [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* assembly [Aspose.Words](../../../)
