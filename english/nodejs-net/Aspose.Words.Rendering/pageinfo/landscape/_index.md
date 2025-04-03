---
title: PageInfo.landscape property
linktitle: landscape property
articleTitle: landscape property
second_title: Aspose.Words for NodeJs
description: "PageInfo.landscape property. Returns ``true`` if the page orientation specified in the document for this page is landscape."
type: docs
weight: 30
url: /nodejs-net/Aspose.Words.Rendering/pageinfo/landscape/
---

## PageInfo.landscape property

Returns ``true`` if the page orientation specified in the document for this page is landscape.



```js
get landscape(): boolean
```

### Examples

Shows how to customize the printing of Aspose.words documents.

```js
let doc = new aw.Document(base.myDir + "Rendering.docx");

  let printDoc = new MyPrintDocument(doc);
  printDoc.printerSettings.PrintRange = System.drawing.printing.PrintRange.SomePages;
  printDoc.printerSettings.FromPage = 1;
  printDoc.printerSettings.ToPage = 1;

  printDoc.print();
});


  /// <summary>
  /// Selects an appropriate paper size, orientation, and paper tray when printing.
  /// </summary>
public class MyPrintDocument : PrintDocument
{
  public MyPrintDocument(Document document)
  {
    mDocument = document;
  }

    /// <summary>
    /// Initializes the range of pages to be printed according to the user selection.
    /// </summary>
  protected override void OnBeginPrint(PrintEventArgs e)
  {
    base.OnBeginPrint(e);

    switch (PrinterSettings.PrintRange)
    {
      case System.drawing.printing.PrintRange.allPages:
        mCurrentPage = 1;
        mPageTo = mDocument.pageCount;
        break;
      case System.drawing.printing.PrintRange.SomePages:
        mCurrentPage = PrinterSettings.FromPage;
        mPageTo = PrinterSettings.ToPage;
        break;
      default:
        throw new InvalidOperationException("Unsupported print range.");
    }
  }

    /// <summary>
    /// Called before each page is printed. 
    /// </summary>
  protected override void OnQueryPageSettings(QueryPageSettingsEventArgs e)
  {
    base.OnQueryPageSettings(e);

      // A single Microsoft Word document can have multiple sections that specify pages with different sizes, 
      // orientations, and paper trays. The .NET printing framework calls this code before 
      // each page is printed, which gives us a chance to specify how to print the current page.
    let pageInfo = mDocument.getPageInfo(mCurrentPage - 1);
    e.PageSettings.paperSize = pageInfo.GetDotNetPaperSize(PrinterSettings.PaperSizes);

      // Microsoft Word stores the paper source (printer tray) for each section as a printer-specific value.
      // To obtain the correct tray value, you will need to use the "RawKind" property, which your printer should return.
    e.PageSettings.PaperSource.RawKind = pageInfo.paperTray;
    e.PageSettings.landscape = pageInfo.landscape;
  }

    /// <summary>
    /// Called for each page to render it for printing. 
    /// </summary>
  protected override void OnPrintPage(PrintPageEventArgs e)
  {
    base.OnPrintPage(e);

      // Aspose.Words rendering engine creates a page drawn from the origin (x = 0, y = 0) of the paper.
      // There will be a hard margin in the printer, which will render each page. We need to offset by that hard margin.
    float hardOffsetX, hardOffsetY;

      // Below are two ways of setting a hard margin.
    if (e.PageSettings != null && e.PageSettings.HardMarginX != 0 && e.PageSettings.HardMarginY != 0)
    {
        // 1 -  Via the "PageSettings" property.
      hardOffsetX = e.PageSettings.HardMarginX;
      hardOffsetY = e.PageSettings.HardMarginY;
    }
    else
    {
        // 2 -  Using our own values, if the "PageSettings" property is unavailable.
      hardOffsetX = 20;
      hardOffsetY = 20;
    }

    mDocument.renderToScale(mCurrentPage, e.Graphics, -hardOffsetX, -hardOffsetY, 1.0f);

    mCurrentPage++;
    e.HasMorePages = mCurrentPage <= mPageTo;
  }

  private readonly Document mDocument;
  private int mCurrentPage;
  private int mPageTo;
}
```

Shows how to print page size and orientation information for every page in a Word document.

```js
let doc = new aw.Document(base.myDir + "Rendering.docx");

// The first section has 2 pages. We will assign a different printer paper tray to each one,
// whose number will match a kind of paper source. These sources and their Kinds will vary
// depending on the installed printer driver.
PrinterSettings.PaperSourceCollection paperSources = new PrinterSettings().PaperSources;

doc.firstSection.pageSetup.firstPageTray = paperSources.at(0).RawKind;
doc.firstSection.pageSetup.otherPagesTray = paperSources.at(1).RawKind;

console.log("Document \"{0}\" contains {1} pages.", doc.originalFileName, doc.pageCount);

float scale = 1.0f;
float dpi = 96;

for (let i = 0; i < doc.pageCount; i++)
{
  // Each page has a PageInfo object, whose index is the respective page's number.
  let pageInfo = doc.getPageInfo(i);

  // Print the page's orientation and dimensions.
  console.log(`Page ${i + 1}:`);
  console.log(`\tOrientation:\t{(pageInfo.landscape ? `Landscape" : "Portrait")}");
  console.log(`\tPaper size:\t\t${pageInfo.paperSize} (${pageInfo.widthInPoints:F0}x${pageInfo.heightInPoints:F0}pt)`);
  console.log(`\tSize in points:\t${pageInfo.sizeInPoints}`);
  console.log(`\tSize in pixels:\t${pageInfo.getSizeInPixels(1.0f, 96)} at ${scale * 100}% scale, ${dpi} dpi`);

  // Print the source tray information.
  console.log(`\tTray:\t${pageInfo.paperTray}`);
  PaperSource source = pageInfo.GetSpecifiedPrinterPaperSource(paperSources, paperSources.at(0));
  console.log(`\tSuitable print source:\t${source.SourceName}, kind: ${source.kind}`);
}
```

### See Also

* module [Aspose.Words.Rendering](../../)
* class [PageInfo](../)

