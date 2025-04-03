---
title: PageSetup.otherPagesTray property
linktitle: otherPagesTray property
articleTitle: otherPagesTray property
second_title: Aspose.Words for NodeJs
description: "PageSetup.otherPagesTray property. Gets or sets the paper tray (bin) to be used for all but the first page of a section"
type: docs
weight: 300
url: /nodejs-net/aspose.words/pagesetup/otherPagesTray/
---

## PageSetup.otherPagesTray property

Gets or sets the paper tray (bin) to be used for all but the first page of a section.
The value is implementation (printer) specific.


```js
get otherPagesTray(): number
```

### Examples

Shows how to get all the sections in a document to use the default paper tray of the selected printer.

```js
let doc = new aw.Document();

// Find the default printer that we will use for printing this document.
// You can define a specific printer using the "PrinterName" property of the PrinterSettings object.
let settings = new PrinterSettings();

// The paper tray value stored in documents is printer specific.
// This means the code below resets all page tray values to use the current printers default tray.
// You can enumerate PrinterSettings.PaperSources to find the other valid paper tray values of the selected printer.
foreach (Section section in doc.sections.OfType<Section>())
{
  section.pageSetup.firstPageTray = settings.DefaultPageSettings.PaperSource.RawKind;
  section.pageSetup.otherPagesTray = settings.DefaultPageSettings.PaperSource.RawKind;
}
```

Shows how to set up printing using different printer trays for different paper sizes.

```js
let doc = new aw.Document();

// Find the default printer that we will use for printing this document.
// You can define a specific printer using the "PrinterName" property of the PrinterSettings object.
let settings = new PrinterSettings();

// This is the tray we will use for pages in the "A4" paper size.
int printerTrayForA4 = settings.PaperSources.at(0).RawKind;

// This is the tray we will use for pages in the "Letter" paper size.
int printerTrayForLetter = settings.PaperSources.at(1).RawKind;

// Modify the PageSettings object of this section to get Microsoft Word to instruct the printer
// to use one of the trays we identified above, depending on this section's paper size.
foreach (Section section in doc.sections.OfType<Section>())
{
  if (section.pageSetup.paperSize == Aspose.words.paperSize.letter)
  {
    section.pageSetup.firstPageTray = printerTrayForLetter;
    section.pageSetup.otherPagesTray = printerTrayForLetter;
  }
  else if (section.pageSetup.paperSize == Aspose.words.paperSize.a4)
  {
    section.pageSetup.firstPageTray = printerTrayForA4;
    section.pageSetup.otherPagesTray = printerTrayForA4;
  }
}
```

### See Also

* module [Aspose.Words](../../)
* class [PageSetup](../)

