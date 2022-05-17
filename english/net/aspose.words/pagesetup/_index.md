---
title: PageSetup
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 4070
url: /net/aspose.words/pagesetup/
---
## PageSetup class

Represents the page setup properties of a section.

```csharp
public class PageSetup
```

## Properties

| Name | Description |
| --- | --- |
| [Bidi](bidi) { get; set; } | Specifies that this section contains bidirectional (complex scripts) text. |
| [BorderAlwaysInFront](borderalwaysinfront) { get; set; } | Specifies where the page border is positioned relative to intersecting texts and objects. |
| [BorderAppliesTo](borderappliesto) { get; set; } | Specifies which pages the page border is printed on. |
| [BorderDistanceFrom](borderdistancefrom) { get; set; } | Gets or sets a value that indicates whether the specified page border is measured from the edge of the page or from the text it surrounds. |
| [Borders](borders) { get; } | Gets a collection of the page borders. |
| [BorderSurroundsFooter](bordersurroundsfooter) { get; set; } | Specifies whether the page border includes or excludes the footer. |
| [BorderSurroundsHeader](bordersurroundsheader) { get; set; } | Specifies whether the page border includes or excludes the header. |
| [BottomMargin](bottommargin) { get; set; } | Returns or sets the distance (in points) between the bottom edge of the page and the bottom boundary of the body text. |
| [ChapterPageSeparator](chapterpageseparator) { get; set; } | Gets or sets the separator character that appears between the chapter number and the page number. |
| [CharactersPerLine](charactersperline) { get; set; } | Gets or sets the number of characters per line in the document grid. |
| [DifferentFirstPageHeaderFooter](differentfirstpageheaderfooter) { get; set; } | **True** if a different header or footer is used on the first page. |
| [EndnoteOptions](endnoteoptions) { get; } | Provides options that control numbering and positioning of endnotes in this section. |
| [FirstPageTray](firstpagetray) { get; set; } | Gets or sets the paper tray (bin) to use for the first page of a section. The value is implementation (printer) specific. |
| [FooterDistance](footerdistance) { get; set; } | Returns or sets the distance (in points) between the footer and the bottom of the page. |
| [FootnoteOptions](footnoteoptions) { get; } | Provides options that control numbering and positioning of footnotes in this section. |
| [Gutter](gutter) { get; set; } | Gets or sets the amount of extra space added to the margin for document binding. |
| [HeaderDistance](headerdistance) { get; set; } | Returns or sets the distance (in points) between the header and the top of the page. |
| [HeadingLevelForChapter](headinglevelforchapter) { get; set; } | Gets or sets the heading level style that is applied to the chapter titles in the document. |
| [LayoutMode](layoutmode) { get; set; } | Gets or sets the layout mode of this section. |
| [LeftMargin](leftmargin) { get; set; } | Returns or sets the distance (in points) between the left edge of the page and the left boundary of the body text. |
| [LineNumberCountBy](linenumbercountby) { get; set; } | Returns or sets the numeric increment for line numbers. |
| [LineNumberDistanceFromText](linenumberdistancefromtext) { get; set; } | Gets or sets distance between the right edge of line numbers and the left edge of the document. |
| [LineNumberRestartMode](linenumberrestartmode) { get; set; } | Gets or sets the way line numbering runs that is, whether it starts over at the beginning of a new page or section or runs continuously. |
| [LinesPerPage](linesperpage) { get; set; } | Gets or sets the number of lines per page in the document grid. |
| [LineStartingNumber](linestartingnumber) { get; set; } | Gets or sets the starting line number. |
| [MultiplePages](multiplepages) { get; set; } | For multiple page documents, gets or sets how a document is printed or rendered so that it can be bound as a booklet. |
| [OddAndEvenPagesHeaderFooter](oddandevenpagesheaderfooter) { get; set; } | **True** if the document has different headers and footers for odd-numbered and even-numbered pages. |
| [Orientation](orientation) { get; set; } | Returns or sets the orientation of the page. |
| [OtherPagesTray](otherpagestray) { get; set; } | Gets or sets the paper tray (bin) to be used for all but the first page of a section. The value is implementation (printer) specific. |
| [PageHeight](pageheight) { get; set; } | Returns or sets the height of the page in points. |
| [PageNumberStyle](pagenumberstyle) { get; set; } | Gets or sets the page number format. |
| [PageStartingNumber](pagestartingnumber) { get; set; } | Gets or sets the starting page number of the section. |
| [PageWidth](pagewidth) { get; set; } | Returns or sets the width of the page in points. |
| [PaperSize](papersize) { get; set; } | Returns or sets the paper size. |
| [RestartPageNumbering](restartpagenumbering) { get; set; } | **True** if page numbering restarts at the beginning of the section. |
| [RightMargin](rightmargin) { get; set; } | Returns or sets the distance (in points) between the right edge of the page and the right boundary of the body text. |
| [RtlGutter](rtlgutter) { get; set; } | Gets or sets whether Microsoft Word uses gutters for the section based on a right-to-left language or a left-to-right language. |
| [SectionStart](sectionstart) { get; set; } | Returns or sets the type of section break for the specified object. |
| [SheetsPerBooklet](sheetsperbooklet) { get; set; } | Returns or sets the number of pages to be included in each booklet. |
| [SuppressEndnotes](suppressendnotes) { get; set; } | **True** if endnotes are printed at the end of the next section that doesn't suppress endnotes. Suppressed endnotes are printed before the endnotes in that section. |
| [TextColumns](textcolumns) { get; } | Returns a collection that represents the set of text columns. |
| [TextOrientation](textorientation) { get; set; } | Allows to specify [`TextOrientation`](./textorientation) for the whole page. Default value is Horizontal |
| [TopMargin](topmargin) { get; set; } | Returns or sets the distance (in points) between the top edge of the page and the top boundary of the body text. |
| [VerticalAlignment](verticalalignment) { get; set; } | Returns or sets the vertical alignment of text on each page in a document or section. |

## Methods

| Name | Description |
| --- | --- |
| [ClearFormatting](clearformatting)() | Resets page setup to default paper size, margins and orientation. |

### Remarks

**PageSetup** object contains all the page setup attributes of a section (left margin, bottom margin, paper size, and so on) as properties.

### See Also

* namespace [Aspose.Words](../../aspose.words)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
