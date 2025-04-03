---
title: PageSetup class
linktitle: PageSetup class
articleTitle: PageSetup class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.PageSetup class. Represents the page setup properties of a section"
type: docs
weight: 960
url: /nodejs-net/aspose.words/pagesetup/
---

## PageSetup class

Represents the page setup properties of a section.
To learn more, visit the [Working with Sections](https://docs.aspose.com/words/nodejs-net/working-with-sections/) documentation article.




### Remarks

[PageSetup](./) object contains all the page setup attributes of a section
(left margin, bottom margin, paper size, and so on) as properties.




### Properties

| Name | Description |
| --- | --- |
| [bidi](./bidi/) | Specifies that this section contains bidirectional (complex scripts) text. |
| [borderAlwaysInFront](./borderAlwaysInFront/) | Specifies where the page border is positioned relative to intersecting texts and objects. |
| [borderAppliesTo](./borderAppliesTo/) | Specifies which pages the page border is printed on. |
| [borderDistanceFrom](./borderDistanceFrom/) | Gets or sets a value that indicates whether the specified page border is measured from the edge of the page or from the text it surrounds. |
| [borderSurroundsFooter](./borderSurroundsFooter/) | Specifies whether the page border includes or excludes the footer. |
| [borderSurroundsHeader](./borderSurroundsHeader/) | Specifies whether the page border includes or excludes the header. |
| [borders](./borders/) | Gets a collection of the page borders. |
| [bottomMargin](./bottomMargin/) | Returns or sets the distance (in points) between the bottom edge of the page and the bottom boundary of the body text. |
| [chapterPageSeparator](./chapterPageSeparator/) | Gets or sets the separator character that appears between the chapter number and the page number. |
| [charactersPerLine](./charactersPerLine/) | Gets or sets the number of characters per line in the document grid. |
| [differentFirstPageHeaderFooter](./differentFirstPageHeaderFooter/) | True if a different header or footer is used on the first page. |
| [endnoteOptions](./endnoteOptions/) | Provides options that control numbering and positioning of endnotes in this section. |
| [firstPageTray](./firstPageTray/) | Gets or sets the paper tray (bin) to use for the first page of a section. The value is implementation (printer) specific. |
| [footerDistance](./footerDistance/) | Returns or sets the distance (in points) between the footer and the bottom of the page. |
| [footnoteOptions](./footnoteOptions/) | Provides options that control numbering and positioning of footnotes in this section. |
| [gutter](./gutter/) | Gets or sets the amount of extra space added to the margin for document binding. |
| [headerDistance](./headerDistance/) | Returns or sets the distance (in points) between the header and the top of the page. |
| [headingLevelForChapter](./headingLevelForChapter/) | Gets or sets the heading level style that is applied to the chapter titles in the document. |
| [layoutMode](./layoutMode/) | Gets or sets the layout mode of this section. |
| [leftMargin](./leftMargin/) | Returns or sets the distance (in points) between the left edge of the page and the left boundary of the body text. |
| [lineNumberCountBy](./lineNumberCountBy/) | Returns or sets the numeric increment for line numbers. |
| [lineNumberDistanceFromText](./lineNumberDistanceFromText/) | Gets or sets distance between the right edge of line numbers and the left edge of the document. |
| [lineNumberRestartMode](./lineNumberRestartMode/) | Gets or sets the way line numbering runs  that is, whether it starts over at the beginning of a new page or section or runs continuously. |
| [lineStartingNumber](./lineStartingNumber/) | Gets or sets the starting line number. |
| [linesPerPage](./linesPerPage/) | Gets or sets the number of lines per page in the document grid. |
| [margins](./margins/) | Returns or sets preset [Margins](../margins/) of the page. |
| [multiplePages](./multiplePages/) | For multiple page documents, gets or sets how a document is printed or rendered so that it can be bound as a booklet. |
| [oddAndEvenPagesHeaderFooter](./oddAndEvenPagesHeaderFooter/) | True if the document has different headers and footers for odd-numbered and even-numbered pages. |
| [orientation](./orientation/) | Returns or sets the orientation of the page. |
| [otherPagesTray](./otherPagesTray/) | Gets or sets the paper tray (bin) to be used for all but the first page of a section. The value is implementation (printer) specific. |
| [pageHeight](./pageHeight/) | Returns or sets the height of the page in points. |
| [pageNumberStyle](./pageNumberStyle/) | Gets or sets the page number format. |
| [pageStartingNumber](./pageStartingNumber/) | Gets or sets the starting page number of the section. |
| [pageWidth](./pageWidth/) | Returns or sets the width of the page in points. |
| [paperSize](./paperSize/) | Returns or sets the paper size. |
| [restartPageNumbering](./restartPageNumbering/) | True if page numbering restarts at the beginning of the section. |
| [rightMargin](./rightMargin/) | Returns or sets the distance (in points) between the right edge of the page and the right boundary of the body text. |
| [rtlGutter](./rtlGutter/) | Gets or sets whether Microsoft Word uses gutters for the section based on a right-to-left language or a left-to-right language. |
| [sectionStart](./sectionStart/) | Returns or sets the type of section break for the specified object. |
| [sheetsPerBooklet](./sheetsPerBooklet/) | Returns or sets the number of pages to be included in each booklet. |
| [suppressEndnotes](./suppressEndnotes/) | True if endnotes are printed at the end of the next section that doesn't suppress endnotes. Suppressed endnotes are printed before the endnotes in that section. |
| [textColumns](./textColumns/) | Returns a collection that represents the set of text columns. |
| [textOrientation](./textOrientation/) | Allows to specify [PageSetup.textOrientation](./textOrientation/) for the whole page. Default value is [TextOrientation.Horizontal](../textorientation/#Horizontal) |
| [topMargin](./topMargin/) | Returns or sets the distance (in points) between the top edge of the page and the top boundary of the body text. |
| [verticalAlignment](./verticalAlignment/) | Returns or sets the vertical alignment of text on each page in a document or section. |

### Methods

| Name | Description |
| --- | --- |
|[ clearFormatting()](./clearFormatting/#default) | Resets page setup to default paper size, margins and orientation. |

### Examples

Shows how to apply and revert page setup settings to sections in a document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Modify the page setup properties for the builder's current section and add text.
builder.pageSetup.orientation = aw.Orientation.Landscape;
builder.pageSetup.verticalAlignment = aw.PageVerticalAlignment.Center;
builder.writeln("This is the first section, which landscape oriented with vertically centered text.");

// If we start a new section using a document builder,
// it will inherit the builder's current page setup properties.
builder.insertBreak(aw.BreakType.SectionBreakNewPage);

expect(doc.sections.at(1).pageSetup.orientation).toEqual(aw.Orientation.Landscape);
expect(doc.sections.at(1).pageSetup.verticalAlignment).toEqual(aw.PageVerticalAlignment.Center);

// We can revert its page setup properties to their default values using the "ClearFormatting" method.
builder.pageSetup.clearFormatting();

expect(doc.sections.at(1).pageSetup.orientation).toEqual(aw.Orientation.Portrait);
expect(doc.sections.at(1).pageSetup.verticalAlignment).toEqual(aw.PageVerticalAlignment.Top);

builder.writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc.save(base.artifactsDir + "PageSetup.clearFormatting.docx");
```

### See Also

* module [Aspose.Words](../)

