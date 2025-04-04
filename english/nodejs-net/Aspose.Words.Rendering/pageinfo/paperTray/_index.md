---
title: PageInfo.paperTray property
linktitle: paperTray property
articleTitle: paperTray property
second_title: Aspose.Words for Node.js
description: "PageInfo.paperTray property. Gets the paper tray (bin) for this page as specified in the document"
type: docs
weight: 50
url: /nodejs-net/aspose.words.rendering/pageinfo/paperTray/
---

## PageInfo.paperTray property

Gets the paper tray (bin) for this page as specified in the document.
The value is implementation (printer) specific.


```js
get paperTray(): number
```

### Examples

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

