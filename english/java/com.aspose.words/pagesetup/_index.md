---
title: PageSetup
second_title: Aspose.Words for Java API Reference
description: Represents the page setup properties of a section.
type: docs
weight: 440
url: /java/com.aspose.words/pagesetup/
---

**Inheritance:**
java.lang.Object
```
public class PageSetup
```

Represents the page setup properties of a section.

To learn more, visit the **Working with Sections** documentation article.

**PageSetup** object contains all the page setup attributes of a section (left margin, bottom margin, paper size, and so on) as properties.
## Methods

| Method | Description |
| --- | --- |
| [clearFormatting()](#clearFormatting--) | Resets page setup to default paper size, margins and orientation. |
| [getOddAndEvenPagesHeaderFooter()](#getOddAndEvenPagesHeaderFooter--) | **True** if the document has different headers and footers for odd-numbered and even-numbered pages. |
| [setOddAndEvenPagesHeaderFooter(boolean value)](#setOddAndEvenPagesHeaderFooter-boolean-) | **True** if the document has different headers and footers for odd-numbered and even-numbered pages. |
| [getDifferentFirstPageHeaderFooter()](#getDifferentFirstPageHeaderFooter--) | **True** if a different header or footer is used on the first page. |
| [setDifferentFirstPageHeaderFooter(boolean value)](#setDifferentFirstPageHeaderFooter-boolean-) | **True** if a different header or footer is used on the first page. |
| [getMultiplePages()](#getMultiplePages--) | For multiple page documents, gets or sets how a document is printed or rendered so that it can be bound as a booklet. |
| [setMultiplePages(int value)](#setMultiplePages-int-) | For multiple page documents, gets or sets how a document is printed or rendered so that it can be bound as a booklet. |
| [getSheetsPerBooklet()](#getSheetsPerBooklet--) | Gets the number of pages to be included in each booklet. |
| [setSheetsPerBooklet(int value)](#setSheetsPerBooklet-int-) | Sets the number of pages to be included in each booklet. |
| [getSectionStart()](#getSectionStart--) | Gets the type of section break for the specified object. |
| [setSectionStart(int value)](#setSectionStart-int-) | Sets the type of section break for the specified object. |
| [getSuppressEndnotes()](#getSuppressEndnotes--) | **True** if endnotes are printed at the end of the next section that doesn't suppress endnotes. |
| [setSuppressEndnotes(boolean value)](#setSuppressEndnotes-boolean-) | **True** if endnotes are printed at the end of the next section that doesn't suppress endnotes. |
| [getVerticalAlignment()](#getVerticalAlignment--) | Gets the vertical alignment of text on each page in a document or section. |
| [setVerticalAlignment(int value)](#setVerticalAlignment-int-) | Sets the vertical alignment of text on each page in a document or section. |
| [getBidi()](#getBidi--) | Specifies that this section contains bidirectional (complex scripts) text. |
| [setBidi(boolean value)](#setBidi-boolean-) | Specifies that this section contains bidirectional (complex scripts) text. |
| [getLayoutMode()](#getLayoutMode--) | Gets the layout mode of this section. |
| [setLayoutMode(int value)](#setLayoutMode-int-) | Sets the layout mode of this section. |
| [getCharactersPerLine()](#getCharactersPerLine--) | Gets the number of characters per line in the document grid. |
| [setCharactersPerLine(int value)](#setCharactersPerLine-int-) | Sets the number of characters per line in the document grid. |
| [getLinesPerPage()](#getLinesPerPage--) | Gets the number of lines per page in the document grid. |
| [setLinesPerPage(int value)](#setLinesPerPage-int-) | Sets the number of lines per page in the document grid. |
| [getPageWidth()](#getPageWidth--) | Gets the width of the page in points. |
| [setPageWidth(double value)](#setPageWidth-double-) | Sets the width of the page in points. |
| [getPageHeight()](#getPageHeight--) | Gets the height of the page in points. |
| [setPageHeight(double value)](#setPageHeight-double-) | Sets the height of the page in points. |
| [getPaperSize()](#getPaperSize--) | Gets the paper size. |
| [setPaperSize(int value)](#setPaperSize-int-) | Sets the paper size. |
| [getOrientation()](#getOrientation--) | Gets the orientation of the page. |
| [setOrientation(int value)](#setOrientation-int-) | Sets the orientation of the page. |
| [getLeftMargin()](#getLeftMargin--) | Gets the distance (in points) between the left edge of the page and the left boundary of the body text. |
| [setLeftMargin(double value)](#setLeftMargin-double-) | Sets the distance (in points) between the left edge of the page and the left boundary of the body text. |
| [getRightMargin()](#getRightMargin--) | Gets the distance (in points) between the right edge of the page and the right boundary of the body text. |
| [setRightMargin(double value)](#setRightMargin-double-) | Sets the distance (in points) between the right edge of the page and the right boundary of the body text. |
| [getTopMargin()](#getTopMargin--) | Gets the distance (in points) between the top edge of the page and the top boundary of the body text. |
| [setTopMargin(double value)](#setTopMargin-double-) | Sets the distance (in points) between the top edge of the page and the top boundary of the body text. |
| [getBottomMargin()](#getBottomMargin--) | Gets the distance (in points) between the bottom edge of the page and the bottom boundary of the body text. |
| [setBottomMargin(double value)](#setBottomMargin-double-) | Sets the distance (in points) between the bottom edge of the page and the bottom boundary of the body text. |
| [getHeaderDistance()](#getHeaderDistance--) | Gets the distance (in points) between the header and the top of the page. |
| [setHeaderDistance(double value)](#setHeaderDistance-double-) | Sets the distance (in points) between the header and the top of the page. |
| [getFooterDistance()](#getFooterDistance--) | Gets the distance (in points) between the footer and the bottom of the page. |
| [setFooterDistance(double value)](#setFooterDistance-double-) | Sets the distance (in points) between the footer and the bottom of the page. |
| [getGutter()](#getGutter--) | Gets the amount of extra space added to the margin for document binding. |
| [setGutter(double value)](#setGutter-double-) | Sets the amount of extra space added to the margin for document binding. |
| [getFirstPageTray()](#getFirstPageTray--) | Gets the paper tray (bin) to use for the first page of a section. |
| [setFirstPageTray(int value)](#setFirstPageTray-int-) | Sets the paper tray (bin) to use for the first page of a section. |
| [getOtherPagesTray()](#getOtherPagesTray--) | Gets the paper tray (bin) to be used for all but the first page of a section. |
| [setOtherPagesTray(int value)](#setOtherPagesTray-int-) | Sets the paper tray (bin) to be used for all but the first page of a section. |
| [getHeadingLevelForChapter()](#getHeadingLevelForChapter--) | Gets the heading level style that is applied to the chapter titles in the document. |
| [setHeadingLevelForChapter(int value)](#setHeadingLevelForChapter-int-) | Sets the heading level style that is applied to the chapter titles in the document. |
| [getChapterPageSeparator()](#getChapterPageSeparator--) | Gets the separator character that appears between the chapter number and the page number. |
| [setChapterPageSeparator(int value)](#setChapterPageSeparator-int-) | Sets the separator character that appears between the chapter number and the page number. |
| [getPageNumberStyle()](#getPageNumberStyle--) | Gets the page number format. |
| [setPageNumberStyle(int value)](#setPageNumberStyle-int-) | Sets the page number format. |
| [getRestartPageNumbering()](#getRestartPageNumbering--) | **True** if page numbering restarts at the beginning of the section. |
| [setRestartPageNumbering(boolean value)](#setRestartPageNumbering-boolean-) | **True** if page numbering restarts at the beginning of the section. |
| [getPageStartingNumber()](#getPageStartingNumber--) | Gets the starting page number of the section. |
| [setPageStartingNumber(int value)](#setPageStartingNumber-int-) | Sets the starting page number of the section. |
| [getLineNumberRestartMode()](#getLineNumberRestartMode--) | Gets the way line numbering runs that is, whether it starts over at the beginning of a new page or section or runs continuously. |
| [setLineNumberRestartMode(int value)](#setLineNumberRestartMode-int-) | Sets the way line numbering runs that is, whether it starts over at the beginning of a new page or section or runs continuously. |
| [getLineNumberCountBy()](#getLineNumberCountBy--) | Gets the numeric increment for line numbers. |
| [setLineNumberCountBy(int value)](#setLineNumberCountBy-int-) | Sets the numeric increment for line numbers. |
| [getLineNumberDistanceFromText()](#getLineNumberDistanceFromText--) | Gets distance between the right edge of line numbers and the left edge of the document. |
| [setLineNumberDistanceFromText(double value)](#setLineNumberDistanceFromText-double-) | Sets distance between the right edge of line numbers and the left edge of the document. |
| [getLineStartingNumber()](#getLineStartingNumber--) | Gets the starting line number. |
| [setLineStartingNumber(int value)](#setLineStartingNumber-int-) | Sets the starting line number. |
| [getTextColumns()](#getTextColumns--) | Returns a collection that represents the set of text columns. |
| [getRtlGutter()](#getRtlGutter--) | Gets whether Microsoft Word uses gutters for the section based on a right-to-left language or a left-to-right language. |
| [setRtlGutter(boolean value)](#setRtlGutter-boolean-) | Sets whether Microsoft Word uses gutters for the section based on a right-to-left language or a left-to-right language. |
| [getBorderAlwaysInFront()](#getBorderAlwaysInFront--) | Specifies where the page border is positioned relative to intersecting texts and objects. |
| [setBorderAlwaysInFront(boolean value)](#setBorderAlwaysInFront-boolean-) | Specifies where the page border is positioned relative to intersecting texts and objects. |
| [getBorderDistanceFrom()](#getBorderDistanceFrom--) | Gets a value that indicates whether the specified page border is measured from the edge of the page or from the text it surrounds. |
| [setBorderDistanceFrom(int value)](#setBorderDistanceFrom-int-) | Sets a value that indicates whether the specified page border is measured from the edge of the page or from the text it surrounds. |
| [getBorderAppliesTo()](#getBorderAppliesTo--) | Specifies which pages the page border is printed on. |
| [setBorderAppliesTo(int value)](#setBorderAppliesTo-int-) | Specifies which pages the page border is printed on. |
| [getBorderSurroundsHeader()](#getBorderSurroundsHeader--) | Specifies whether the page border includes or excludes the header. |
| [setBorderSurroundsHeader(boolean value)](#setBorderSurroundsHeader-boolean-) | Specifies whether the page border includes or excludes the header. |
| [getBorderSurroundsFooter()](#getBorderSurroundsFooter--) | Specifies whether the page border includes or excludes the footer. |
| [setBorderSurroundsFooter(boolean value)](#setBorderSurroundsFooter-boolean-) | Specifies whether the page border includes or excludes the footer. |
| [getBorders()](#getBorders--) | Gets a collection of the page borders. |
| [getFootnoteOptions()](#getFootnoteOptions--) | Provides options that control numbering and positioning of footnotes in this section. |
| [getEndnoteOptions()](#getEndnoteOptions--) | Provides options that control numbering and positioning of endnotes in this section. |
| [getTextOrientation()](#getTextOrientation--) | Allows to specify [getTextOrientation()](../../com.aspose.words/pagesetup\#getTextOrientation--) / [setTextOrientation(int)](../../com.aspose.words/pagesetup\#setTextOrientation-int-) for the whole page. |
| [setTextOrientation(int value)](#setTextOrientation-int-) | Allows to specify [getTextOrientation()](../../com.aspose.words/pagesetup\#getTextOrientation--) / [setTextOrientation(int)](../../com.aspose.words/pagesetup\#setTextOrientation-int-) for the whole page. |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int-) |  |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int-) |  |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object-) |  |
### clearFormatting() {#clearFormatting--}
```
public void clearFormatting()
```


Resets page setup to default paper size, margins and orientation.

### getOddAndEvenPagesHeaderFooter() {#getOddAndEvenPagesHeaderFooter--}
```
public boolean getOddAndEvenPagesHeaderFooter()
```


**True** if the document has different headers and footers for odd-numbered and even-numbered pages. Note, changing this property affects all sections in the document.

**Returns:**
boolean - The corresponding  boolean  value.
### setOddAndEvenPagesHeaderFooter(boolean value) {#setOddAndEvenPagesHeaderFooter-boolean-}
```
public void setOddAndEvenPagesHeaderFooter(boolean value)
```


**True** if the document has different headers and footers for odd-numbered and even-numbered pages. Note, changing this property affects all sections in the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getDifferentFirstPageHeaderFooter() {#getDifferentFirstPageHeaderFooter--}
```
public boolean getDifferentFirstPageHeaderFooter()
```


**True** if a different header or footer is used on the first page.

**Returns:**
boolean - The corresponding  boolean  value.
### setDifferentFirstPageHeaderFooter(boolean value) {#setDifferentFirstPageHeaderFooter-boolean-}
```
public void setDifferentFirstPageHeaderFooter(boolean value)
```


**True** if a different header or footer is used on the first page.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getMultiplePages() {#getMultiplePages--}
```
public int getMultiplePages()
```


For multiple page documents, gets or sets how a document is printed or rendered so that it can be bound as a booklet.

**Returns:**
int - The corresponding  int  value. The returned value is one of [MultiplePagesType](../../com.aspose.words/multiplepagestype) constants.
### setMultiplePages(int value) {#setMultiplePages-int-}
```
public void setMultiplePages(int value)
```


For multiple page documents, gets or sets how a document is printed or rendered so that it can be bound as a booklet.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [MultiplePagesType](../../com.aspose.words/multiplepagestype) constants. |

### getSheetsPerBooklet() {#getSheetsPerBooklet--}
```
public int getSheetsPerBooklet()
```


Gets the number of pages to be included in each booklet.

**Returns:**
int - The number of pages to be included in each booklet.
### setSheetsPerBooklet(int value) {#setSheetsPerBooklet-int-}
```
public void setSheetsPerBooklet(int value)
```


Sets the number of pages to be included in each booklet.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The number of pages to be included in each booklet. |

### getSectionStart() {#getSectionStart--}
```
public int getSectionStart()
```


Gets the type of section break for the specified object.

**Returns:**
int - The type of section break for the specified object. The returned value is one of [SectionStart](../../com.aspose.words/sectionstart) constants.
### setSectionStart(int value) {#setSectionStart-int-}
```
public void setSectionStart(int value)
```


Sets the type of section break for the specified object.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The type of section break for the specified object. The value must be one of [SectionStart](../../com.aspose.words/sectionstart) constants. |

### getSuppressEndnotes() {#getSuppressEndnotes--}
```
public boolean getSuppressEndnotes()
```


**True** if endnotes are printed at the end of the next section that doesn't suppress endnotes. Suppressed endnotes are printed before the endnotes in that section.

**Returns:**
boolean - The corresponding  boolean  value.
### setSuppressEndnotes(boolean value) {#setSuppressEndnotes-boolean-}
```
public void setSuppressEndnotes(boolean value)
```


**True** if endnotes are printed at the end of the next section that doesn't suppress endnotes. Suppressed endnotes are printed before the endnotes in that section.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getVerticalAlignment() {#getVerticalAlignment--}
```
public int getVerticalAlignment()
```


Gets the vertical alignment of text on each page in a document or section.

**Returns:**
int - The vertical alignment of text on each page in a document or section. The returned value is one of [PageVerticalAlignment](../../com.aspose.words/pageverticalalignment) constants.
### setVerticalAlignment(int value) {#setVerticalAlignment-int-}
```
public void setVerticalAlignment(int value)
```


Sets the vertical alignment of text on each page in a document or section.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The vertical alignment of text on each page in a document or section. The value must be one of [PageVerticalAlignment](../../com.aspose.words/pageverticalalignment) constants. |

### getBidi() {#getBidi--}
```
public boolean getBidi()
```


Specifies that this section contains bidirectional (complex scripts) text.

When true, the columns in this section are laid out from right to left.

**Returns:**
boolean - The corresponding  boolean  value.
### setBidi(boolean value) {#setBidi-boolean-}
```
public void setBidi(boolean value)
```


Specifies that this section contains bidirectional (complex scripts) text.

When true, the columns in this section are laid out from right to left.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getLayoutMode() {#getLayoutMode--}
```
public int getLayoutMode()
```


Gets the layout mode of this section.

**Returns:**
int - The layout mode of this section. The returned value is one of [SectionLayoutMode](../../com.aspose.words/sectionlayoutmode) constants.
### setLayoutMode(int value) {#setLayoutMode-int-}
```
public void setLayoutMode(int value)
```


Sets the layout mode of this section.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The layout mode of this section. The value must be one of [SectionLayoutMode](../../com.aspose.words/sectionlayoutmode) constants. |

### getCharactersPerLine() {#getCharactersPerLine--}
```
public int getCharactersPerLine()
```


Gets the number of characters per line in the document grid.

Minimum value of the property is 1. Maximum value depends on page width and font size of the Normal style. Minimum character pitch is 90 percent of the font size. For example, maximum number of characters per line of a Letter page with one-inch margins is 43.

By default, the property has a value, on which character pitch equals to font size of the Normal style.

**Returns:**
int - The number of characters per line in the document grid.
### setCharactersPerLine(int value) {#setCharactersPerLine-int-}
```
public void setCharactersPerLine(int value)
```


Sets the number of characters per line in the document grid.

Minimum value of the property is 1. Maximum value depends on page width and font size of the Normal style. Minimum character pitch is 90 percent of the font size. For example, maximum number of characters per line of a Letter page with one-inch margins is 43.

By default, the property has a value, on which character pitch equals to font size of the Normal style.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The number of characters per line in the document grid. |

### getLinesPerPage() {#getLinesPerPage--}
```
public int getLinesPerPage()
```


Gets the number of lines per page in the document grid.

Minimum value of the property is 1. Maximum value depends on page height and font size of the Normal style. Minimum line pitch is 136 percent of the font size. For example, maximum number of lines per page of a Letter page with one-inch margins is 39.

By default, the property has a value, on which line pitch is in 1.5 times greater than font size of the Normal style.

**Returns:**
int - The number of lines per page in the document grid.
### setLinesPerPage(int value) {#setLinesPerPage-int-}
```
public void setLinesPerPage(int value)
```


Sets the number of lines per page in the document grid.

Minimum value of the property is 1. Maximum value depends on page height and font size of the Normal style. Minimum line pitch is 136 percent of the font size. For example, maximum number of lines per page of a Letter page with one-inch margins is 39.

By default, the property has a value, on which line pitch is in 1.5 times greater than font size of the Normal style.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The number of lines per page in the document grid. |

### getPageWidth() {#getPageWidth--}
```
public double getPageWidth()
```


Gets the width of the page in points.

**Returns:**
double - The width of the page in points.
### setPageWidth(double value) {#setPageWidth-double-}
```
public void setPageWidth(double value)
```


Sets the width of the page in points.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The width of the page in points. |

### getPageHeight() {#getPageHeight--}
```
public double getPageHeight()
```


Gets the height of the page in points.

**Returns:**
double - The height of the page in points.
### setPageHeight(double value) {#setPageHeight-double-}
```
public void setPageHeight(double value)
```


Sets the height of the page in points.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The height of the page in points. |

### getPaperSize() {#getPaperSize--}
```
public int getPaperSize()
```


Gets the paper size.

Setting this property updates [getPageWidth()](../../com.aspose.words/pagesetup\#getPageWidth--) / [setPageWidth(double)](../../com.aspose.words/pagesetup\#setPageWidth-double-) and [getPageHeight()](../../com.aspose.words/pagesetup\#getPageHeight--) / [setPageHeight(double)](../../com.aspose.words/pagesetup\#setPageHeight-double-) values. Setting this value to [PaperSize.CUSTOM](../../com.aspose.words/papersize\#CUSTOM) does not change existing values.

**Returns:**
int - The paper size. The returned value is one of [PaperSize](../../com.aspose.words/papersize) constants.
### setPaperSize(int value) {#setPaperSize-int-}
```
public void setPaperSize(int value)
```


Sets the paper size.

Setting this property updates [getPageWidth()](../../com.aspose.words/pagesetup\#getPageWidth--) / [setPageWidth(double)](../../com.aspose.words/pagesetup\#setPageWidth-double-) and [getPageHeight()](../../com.aspose.words/pagesetup\#getPageHeight--) / [setPageHeight(double)](../../com.aspose.words/pagesetup\#setPageHeight-double-) values. Setting this value to [PaperSize.CUSTOM](../../com.aspose.words/papersize\#CUSTOM) does not change existing values.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The paper size. The value must be one of [PaperSize](../../com.aspose.words/papersize) constants. |

### getOrientation() {#getOrientation--}
```
public int getOrientation()
```


Gets the orientation of the page.

Changing **Orientation** swaps [getPageWidth()](../../com.aspose.words/pagesetup\#getPageWidth--) / [setPageWidth(double)](../../com.aspose.words/pagesetup\#setPageWidth-double-) and [getPageHeight()](../../com.aspose.words/pagesetup\#getPageHeight--) / [setPageHeight(double)](../../com.aspose.words/pagesetup\#setPageHeight-double-).

**Returns:**
int - The orientation of the page. The returned value is one of [Orientation](../../com.aspose.words/orientation) constants.
### setOrientation(int value) {#setOrientation-int-}
```
public void setOrientation(int value)
```


Sets the orientation of the page.

Changing **Orientation** swaps [getPageWidth()](../../com.aspose.words/pagesetup\#getPageWidth--) / [setPageWidth(double)](../../com.aspose.words/pagesetup\#setPageWidth-double-) and [getPageHeight()](../../com.aspose.words/pagesetup\#getPageHeight--) / [setPageHeight(double)](../../com.aspose.words/pagesetup\#setPageHeight-double-).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The orientation of the page. The value must be one of [Orientation](../../com.aspose.words/orientation) constants. |

### getLeftMargin() {#getLeftMargin--}
```
public double getLeftMargin()
```


Gets the distance (in points) between the left edge of the page and the left boundary of the body text.

**Returns:**
double - The distance (in points) between the left edge of the page and the left boundary of the body text.
### setLeftMargin(double value) {#setLeftMargin-double-}
```
public void setLeftMargin(double value)
```


Sets the distance (in points) between the left edge of the page and the left boundary of the body text.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The distance (in points) between the left edge of the page and the left boundary of the body text. |

### getRightMargin() {#getRightMargin--}
```
public double getRightMargin()
```


Gets the distance (in points) between the right edge of the page and the right boundary of the body text.

**Returns:**
double - The distance (in points) between the right edge of the page and the right boundary of the body text.
### setRightMargin(double value) {#setRightMargin-double-}
```
public void setRightMargin(double value)
```


Sets the distance (in points) between the right edge of the page and the right boundary of the body text.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The distance (in points) between the right edge of the page and the right boundary of the body text. |

### getTopMargin() {#getTopMargin--}
```
public double getTopMargin()
```


Gets the distance (in points) between the top edge of the page and the top boundary of the body text.

**Returns:**
double - The distance (in points) between the top edge of the page and the top boundary of the body text.
### setTopMargin(double value) {#setTopMargin-double-}
```
public void setTopMargin(double value)
```


Sets the distance (in points) between the top edge of the page and the top boundary of the body text.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The distance (in points) between the top edge of the page and the top boundary of the body text. |

### getBottomMargin() {#getBottomMargin--}
```
public double getBottomMargin()
```


Gets the distance (in points) between the bottom edge of the page and the bottom boundary of the body text.

**Returns:**
double - The distance (in points) between the bottom edge of the page and the bottom boundary of the body text.
### setBottomMargin(double value) {#setBottomMargin-double-}
```
public void setBottomMargin(double value)
```


Sets the distance (in points) between the bottom edge of the page and the bottom boundary of the body text.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The distance (in points) between the bottom edge of the page and the bottom boundary of the body text. |

### getHeaderDistance() {#getHeaderDistance--}
```
public double getHeaderDistance()
```


Gets the distance (in points) between the header and the top of the page.

**Returns:**
double - The distance (in points) between the header and the top of the page.
### setHeaderDistance(double value) {#setHeaderDistance-double-}
```
public void setHeaderDistance(double value)
```


Sets the distance (in points) between the header and the top of the page.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The distance (in points) between the header and the top of the page. |

### getFooterDistance() {#getFooterDistance--}
```
public double getFooterDistance()
```


Gets the distance (in points) between the footer and the bottom of the page.

**Returns:**
double - The distance (in points) between the footer and the bottom of the page.
### setFooterDistance(double value) {#setFooterDistance-double-}
```
public void setFooterDistance(double value)
```


Sets the distance (in points) between the footer and the bottom of the page.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The distance (in points) between the footer and the bottom of the page. |

### getGutter() {#getGutter--}
```
public double getGutter()
```


Gets the amount of extra space added to the margin for document binding.

**Returns:**
double - The amount of extra space added to the margin for document binding.
### setGutter(double value) {#setGutter-double-}
```
public void setGutter(double value)
```


Sets the amount of extra space added to the margin for document binding.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The amount of extra space added to the margin for document binding. |

### getFirstPageTray() {#getFirstPageTray--}
```
public int getFirstPageTray()
```


Gets the paper tray (bin) to use for the first page of a section. The value is implementation (printer) specific.

**Returns:**
int - The paper tray (bin) to use for the first page of a section.
### setFirstPageTray(int value) {#setFirstPageTray-int-}
```
public void setFirstPageTray(int value)
```


Sets the paper tray (bin) to use for the first page of a section. The value is implementation (printer) specific.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The paper tray (bin) to use for the first page of a section. |

### getOtherPagesTray() {#getOtherPagesTray--}
```
public int getOtherPagesTray()
```


Gets the paper tray (bin) to be used for all but the first page of a section. The value is implementation (printer) specific.

**Returns:**
int - The paper tray (bin) to be used for all but the first page of a section.
### setOtherPagesTray(int value) {#setOtherPagesTray-int-}
```
public void setOtherPagesTray(int value)
```


Sets the paper tray (bin) to be used for all but the first page of a section. The value is implementation (printer) specific.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The paper tray (bin) to be used for all but the first page of a section. |

### getHeadingLevelForChapter() {#getHeadingLevelForChapter--}
```
public int getHeadingLevelForChapter()
```


Gets the heading level style that is applied to the chapter titles in the document.

Can be a number from 0 through 9. 0 means no chapter number if applied to page number.

Before you can create page numbers that include chapter numbers, the document headings must have a numbered outline format applied.

**Returns:**
int - The heading level style that is applied to the chapter titles in the document.
### setHeadingLevelForChapter(int value) {#setHeadingLevelForChapter-int-}
```
public void setHeadingLevelForChapter(int value)
```


Sets the heading level style that is applied to the chapter titles in the document.

Can be a number from 0 through 9. 0 means no chapter number if applied to page number.

Before you can create page numbers that include chapter numbers, the document headings must have a numbered outline format applied.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The heading level style that is applied to the chapter titles in the document. |

### getChapterPageSeparator() {#getChapterPageSeparator--}
```
public int getChapterPageSeparator()
```


Gets the separator character that appears between the chapter number and the page number.

Before you can create page numbers that include chapter numbers, the document headings must have a numbered outline format applied.

**Returns:**
int - The separator character that appears between the chapter number and the page number. The returned value is one of [ChapterPageSeparator](../../com.aspose.words/chapterpageseparator) constants.
### setChapterPageSeparator(int value) {#setChapterPageSeparator-int-}
```
public void setChapterPageSeparator(int value)
```


Sets the separator character that appears between the chapter number and the page number.

Before you can create page numbers that include chapter numbers, the document headings must have a numbered outline format applied.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The separator character that appears between the chapter number and the page number. The value must be one of [ChapterPageSeparator](../../com.aspose.words/chapterpageseparator) constants. |

### getPageNumberStyle() {#getPageNumberStyle--}
```
public int getPageNumberStyle()
```


Gets the page number format.

**Returns:**
int - The page number format. The returned value is one of [NumberStyle](../../com.aspose.words/numberstyle) constants.
### setPageNumberStyle(int value) {#setPageNumberStyle-int-}
```
public void setPageNumberStyle(int value)
```


Sets the page number format.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The page number format. The value must be one of [NumberStyle](../../com.aspose.words/numberstyle) constants. |

### getRestartPageNumbering() {#getRestartPageNumbering--}
```
public boolean getRestartPageNumbering()
```


**True** if page numbering restarts at the beginning of the section. If set to **false**, the **RestartPageNumbering** property will override the [getPageStartingNumber()](../../com.aspose.words/pagesetup\#getPageStartingNumber--) / [setPageStartingNumber(int)](../../com.aspose.words/pagesetup\#setPageStartingNumber-int-) property so that page numbering can continue from the previous section.

**Returns:**
boolean - The corresponding  boolean  value.
### setRestartPageNumbering(boolean value) {#setRestartPageNumbering-boolean-}
```
public void setRestartPageNumbering(boolean value)
```


**True** if page numbering restarts at the beginning of the section. If set to **false**, the **RestartPageNumbering** property will override the [getPageStartingNumber()](../../com.aspose.words/pagesetup\#getPageStartingNumber--) / [setPageStartingNumber(int)](../../com.aspose.words/pagesetup\#setPageStartingNumber-int-) property so that page numbering can continue from the previous section.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getPageStartingNumber() {#getPageStartingNumber--}
```
public int getPageStartingNumber()
```


Gets the starting page number of the section. The [getRestartPageNumbering()](../../com.aspose.words/pagesetup\#getRestartPageNumbering--) / [setRestartPageNumbering(boolean)](../../com.aspose.words/pagesetup\#setRestartPageNumbering-boolean-) property, if set to **false**, will override the **PageStartingNumber** property so that page numbering can continue from the previous section.

**Returns:**
int - The starting page number of the section.
### setPageStartingNumber(int value) {#setPageStartingNumber-int-}
```
public void setPageStartingNumber(int value)
```


Sets the starting page number of the section. The [getRestartPageNumbering()](../../com.aspose.words/pagesetup\#getRestartPageNumbering--) / [setRestartPageNumbering(boolean)](../../com.aspose.words/pagesetup\#setRestartPageNumbering-boolean-) property, if set to **false**, will override the **PageStartingNumber** property so that page numbering can continue from the previous section.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The starting page number of the section. |

### getLineNumberRestartMode() {#getLineNumberRestartMode--}
```
public int getLineNumberRestartMode()
```


Gets the way line numbering runs that is, whether it starts over at the beginning of a new page or section or runs continuously.

**Returns:**
int - The way line numbering runs that is, whether it starts over at the beginning of a new page or section or runs continuously. The returned value is one of [LineNumberRestartMode](../../com.aspose.words/linenumberrestartmode) constants.
### setLineNumberRestartMode(int value) {#setLineNumberRestartMode-int-}
```
public void setLineNumberRestartMode(int value)
```


Sets the way line numbering runs that is, whether it starts over at the beginning of a new page or section or runs continuously.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The way line numbering runs that is, whether it starts over at the beginning of a new page or section or runs continuously. The value must be one of [LineNumberRestartMode](../../com.aspose.words/linenumberrestartmode) constants. |

### getLineNumberCountBy() {#getLineNumberCountBy--}
```
public int getLineNumberCountBy()
```


Gets the numeric increment for line numbers.

**Returns:**
int - The numeric increment for line numbers.
### setLineNumberCountBy(int value) {#setLineNumberCountBy-int-}
```
public void setLineNumberCountBy(int value)
```


Sets the numeric increment for line numbers.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The numeric increment for line numbers. |

### getLineNumberDistanceFromText() {#getLineNumberDistanceFromText--}
```
public double getLineNumberDistanceFromText()
```


Gets distance between the right edge of line numbers and the left edge of the document. Set this property to zero for automatic distance between the line numbers and text of the document.

**Returns:**
double - Distance between the right edge of line numbers and the left edge of the document.
### setLineNumberDistanceFromText(double value) {#setLineNumberDistanceFromText-double-}
```
public void setLineNumberDistanceFromText(double value)
```


Sets distance between the right edge of line numbers and the left edge of the document. Set this property to zero for automatic distance between the line numbers and text of the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | Distance between the right edge of line numbers and the left edge of the document. |

### getLineStartingNumber() {#getLineStartingNumber--}
```
public int getLineStartingNumber()
```


Gets the starting line number.

**Returns:**
int - The starting line number.
### setLineStartingNumber(int value) {#setLineStartingNumber-int-}
```
public void setLineStartingNumber(int value)
```


Sets the starting line number.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The starting line number. |

### getTextColumns() {#getTextColumns--}
```
public TextColumnCollection getTextColumns()
```


Returns a collection that represents the set of text columns.

**Returns:**
[TextColumnCollection](../../com.aspose.words/textcolumncollection) - A collection that represents the set of text columns.
### getRtlGutter() {#getRtlGutter--}
```
public boolean getRtlGutter()
```


Gets whether Microsoft Word uses gutters for the section based on a right-to-left language or a left-to-right language.

**Returns:**
boolean - Whether Microsoft Word uses gutters for the section based on a right-to-left language or a left-to-right language.
### setRtlGutter(boolean value) {#setRtlGutter-boolean-}
```
public void setRtlGutter(boolean value)
```


Sets whether Microsoft Word uses gutters for the section based on a right-to-left language or a left-to-right language.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether Microsoft Word uses gutters for the section based on a right-to-left language or a left-to-right language. |

### getBorderAlwaysInFront() {#getBorderAlwaysInFront--}
```
public boolean getBorderAlwaysInFront()
```


Specifies where the page border is positioned relative to intersecting texts and objects.

**Returns:**
boolean - The corresponding  boolean  value.
### setBorderAlwaysInFront(boolean value) {#setBorderAlwaysInFront-boolean-}
```
public void setBorderAlwaysInFront(boolean value)
```


Specifies where the page border is positioned relative to intersecting texts and objects.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getBorderDistanceFrom() {#getBorderDistanceFrom--}
```
public int getBorderDistanceFrom()
```


Gets a value that indicates whether the specified page border is measured from the edge of the page or from the text it surrounds.

**Returns:**
int - A value that indicates whether the specified page border is measured from the edge of the page or from the text it surrounds. The returned value is one of [PageBorderDistanceFrom](../../com.aspose.words/pageborderdistancefrom) constants.
### setBorderDistanceFrom(int value) {#setBorderDistanceFrom-int-}
```
public void setBorderDistanceFrom(int value)
```


Sets a value that indicates whether the specified page border is measured from the edge of the page or from the text it surrounds.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value that indicates whether the specified page border is measured from the edge of the page or from the text it surrounds. The value must be one of [PageBorderDistanceFrom](../../com.aspose.words/pageborderdistancefrom) constants. |

### getBorderAppliesTo() {#getBorderAppliesTo--}
```
public int getBorderAppliesTo()
```


Specifies which pages the page border is printed on.

**Returns:**
int - The corresponding  int  value. The returned value is one of [PageBorderAppliesTo](../../com.aspose.words/pageborderappliesto) constants.
### setBorderAppliesTo(int value) {#setBorderAppliesTo-int-}
```
public void setBorderAppliesTo(int value)
```


Specifies which pages the page border is printed on.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [PageBorderAppliesTo](../../com.aspose.words/pageborderappliesto) constants. |

### getBorderSurroundsHeader() {#getBorderSurroundsHeader--}
```
public boolean getBorderSurroundsHeader()
```


Specifies whether the page border includes or excludes the header. Note, changing this property affects all sections in the document.

**Returns:**
boolean - The corresponding  boolean  value.
### setBorderSurroundsHeader(boolean value) {#setBorderSurroundsHeader-boolean-}
```
public void setBorderSurroundsHeader(boolean value)
```


Specifies whether the page border includes or excludes the header. Note, changing this property affects all sections in the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getBorderSurroundsFooter() {#getBorderSurroundsFooter--}
```
public boolean getBorderSurroundsFooter()
```


Specifies whether the page border includes or excludes the footer. Note, changing this property affects all sections in the document.

**Returns:**
boolean - The corresponding  boolean  value.
### setBorderSurroundsFooter(boolean value) {#setBorderSurroundsFooter-boolean-}
```
public void setBorderSurroundsFooter(boolean value)
```


Specifies whether the page border includes or excludes the footer. Note, changing this property affects all sections in the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getBorders() {#getBorders--}
```
public BorderCollection getBorders()
```


Gets a collection of the page borders.

**Returns:**
[BorderCollection](../../com.aspose.words/bordercollection) - A collection of the page borders.
### getFootnoteOptions() {#getFootnoteOptions--}
```
public FootnoteOptions getFootnoteOptions()
```


Provides options that control numbering and positioning of footnotes in this section.

**Returns:**
[FootnoteOptions](../../com.aspose.words/footnoteoptions) - The corresponding [FootnoteOptions](../../com.aspose.words/footnoteoptions) value.
### getEndnoteOptions() {#getEndnoteOptions--}
```
public EndnoteOptions getEndnoteOptions()
```


Provides options that control numbering and positioning of endnotes in this section.

**Returns:**
[EndnoteOptions](../../com.aspose.words/endnoteoptions) - The corresponding [EndnoteOptions](../../com.aspose.words/endnoteoptions) value.
### getTextOrientation() {#getTextOrientation--}
```
public int getTextOrientation()
```


Allows to specify [getTextOrientation()](../../com.aspose.words/pagesetup\#getTextOrientation--) / [setTextOrientation(int)](../../com.aspose.words/pagesetup\#setTextOrientation-int-) for the whole page. Default value is [TextOrientation.HORIZONTAL](../../com.aspose.words/textorientation\#HORIZONTAL) This property is only supported for MS Word native formats DOCX, WML, RTF and DOC.

**Returns:**
int - The corresponding  int  value. The returned value is one of [TextOrientation](../../com.aspose.words/textorientation) constants.
### setTextOrientation(int value) {#setTextOrientation-int-}
```
public void setTextOrientation(int value)
```


Allows to specify [getTextOrientation()](../../com.aspose.words/pagesetup\#getTextOrientation--) / [setTextOrientation(int)](../../com.aspose.words/pagesetup\#setTextOrientation-int-) for the whole page. Default value is [TextOrientation.HORIZONTAL](../../com.aspose.words/textorientation\#HORIZONTAL) This property is only supported for MS Word native formats DOCX, WML, RTF and DOC.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [TextOrientation](../../com.aspose.words/textorientation) constants. |

### getDirectBorderAttr(int key) {#getDirectBorderAttr-int-}
```
public Object getDirectBorderAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedBorderAttr(int key) {#fetchInheritedBorderAttr-int-}
```
public Object fetchInheritedBorderAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### setBorderAttr(int key, Object value) {#setBorderAttr-int-java.lang.Object-}
```
public void setBorderAttr(int key, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

