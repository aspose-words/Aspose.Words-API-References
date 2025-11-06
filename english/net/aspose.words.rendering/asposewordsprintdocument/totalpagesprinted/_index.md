---
title: AsposeWordsPrintDocument.TotalPagesPrinted
linktitle: TotalPagesPrinted
articleTitle: TotalPagesPrinted
second_title: Aspose.Words for .NET
description: Shows total pages printed in Aspose.Words to track print session output.
type: docs
weight: 60
url: /net/aspose.words.rendering/asposewordsprintdocument/totalpagesprinted/
---
## AsposeWordsPrintDocument.TotalPagesPrinted property

Gets the total number of pages actually printed during the print session.

```csharp
public int TotalPagesPrinted { get; }
```

## Remarks

Updated after printing completes. Returns 0 before printing starts.

## Examples

Shows how to filtering pages base on page color.

```csharp
public void ColorMode()
{
    // Load the document with 3 color pages and 2 black and white pages.
    Document doc = new Document(MyDir + "Colored pages.docx");

    // Print color pages to 'color' printer.
    int colorPagesPrinted = PrintPages(doc, "Microsoft Print to PDF", true);

    // Print black-and-white pages to 'black-and-white' printer.
    int nonColorPagesPrinted = PrintPages(doc, "Microsoft XPS Document Writer", false);

    // Verify that correct number of pages were printed in each case.
    Assert.That(colorPagesPrinted, Is.EqualTo(3));
    Assert.That(nonColorPagesPrinted, Is.EqualTo(3));
}

/// <summary>
/// Prints document pages filtered by color requirements.
/// </summary>
/// <param name="doc">The document to print.</param>
/// <param name="printerName">The name of the target printer.</param>
/// <param name="colored">
/// <c>true</c> to print only color pages; 
/// <c>false</c> to print only black and white pages.
/// </param>
/// <returns>The number of pages actually printed.</returns>
private int PrintPages(Document doc, string printerName, bool colored)
{
    // Configure printer settings.
    PrinterSettings printerSettings = new PrinterSettings();
    printerSettings.PrinterName = printerName;
    printerSettings.FromPage = 1;
    printerSettings.ToPage = doc.PageCount;

    // Create print document with color mode set to Normal.
    AsposeWordsPrintDocument printDoc = new AsposeWordsPrintDocument(doc);
    printDoc.PrinterSettings = printerSettings;
    printDoc.ColorMode = ColorPrintMode.Normal;

    // Filter pages: skip color pages when printing black and white, and vice versa.
    printDoc.PageIndexFilter = new ColorPagesFilter(doc, !colored);

    printDoc.Print();

    return printDoc.TotalPagesPrinted;
}

/// <summary>
/// A filter that selectively skips color or black-and-white pages during printing
/// based on the document's page information and specified filtering mode.
/// </summary>
/// <remarks>
/// This filter implements the IIndexFilter interface to provide custom page selection
/// logic for printing operations. It can be configured to either skip color pages
/// (when printing only black-and-white content) or skip black-and-white pages
/// (when printing only color content).
/// </remarks>
internal class ColorPagesFilter : IIndexFilter
{
    private readonly Document _doc;
    private readonly bool _skipColorPages;

    /// <summary>
    /// Initializes a new instance of the ColorPagesFilter class.
    /// </summary>
    /// <param name="doc">The document containing page information.</param>
    /// <param name="skipColorPages">
    /// If true, the filter will skip color pages (print only black-and-white pages).
    /// If false, the filter will skip black-and-white pages (print only color pages).
    /// </param>
    public ColorPagesFilter(Document doc, bool skipColorPages)
    {
        _doc = doc;
        _skipColorPages = skipColorPages;
    }

    /// <summary>
    /// Determines whether the page at the specified index should be skipped during printing.
    /// </summary>
    /// <param name="index">The zero-based page index to check.</param>
    /// <returns>
    /// true if the page should be skipped; otherwise, false.
    /// The decision is based on the page's color information and the filter configuration:
    /// - Returns true when the page's color status matches the skip condition.
    /// - Returns false when the page should be printed.
    /// </returns>
    public bool ShouldSkipIndex(int index)
    {
        return _skipColorPages == _doc.GetPageInfo(index).Colored;
    }
}
```

### See Also

* class [AsposeWordsPrintDocument](../)
* namespace [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* assembly [Aspose.Words](../../../)
