---
title: PageSetup
second_title: Aspose.Words for Java API Reference
description: 表示部分的页面设置属性。
type: docs
weight: 440
url: /zh/java/com.aspose.words/pagesetup/
---

**遗产:**
java.lang.Object
```
public class PageSetup
```

表示部分的页面设置属性。

要了解更多信息，请访问**Working with Sections**文档文章。

**PageSetup**对象包含一个部分的所有页面设置属性（左边距、下边距、纸张大小等）作为属性。
## 方法

| 方法 | 描述 |
| --- | --- |
| [clearFormatting()](#clearFormatting--) | 将页面设置重置为默认纸张尺寸、边距和方向。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int-) |  |
| [getBidi()](#getBidi--) | 指定此部分包含双向（复杂脚本）文本。 |
| [getBorderAlwaysInFront()](#getBorderAlwaysInFront--) | 指定页面边框相对于相交文本和对象的位置。 |
| [getBorderAppliesTo()](#getBorderAppliesTo--) | 指定打印页面边框的页面。 |
| [getBorderDistanceFrom()](#getBorderDistanceFrom--) | 获取一个值，该值指示指定的页面边框是从页面边缘还是从其周围的文本测量的。 |
| [getBorderSurroundsFooter()](#getBorderSurroundsFooter--) | 指定页面边框是包括还是不包括页脚。 |
| [getBorderSurroundsHeader()](#getBorderSurroundsHeader--) | 指定页面边框是包括还是不包括页眉。 |
| [getBorders()](#getBorders--) | 获取页面边框的集合。 |
| [getBottomMargin()](#getBottomMargin--) | 获取页面底部边缘和正文底部边界之间的距离（以磅为单位）。 |
| [getChapterPageSeparator()](#getChapterPageSeparator--) | 获取出现在章节号和页码之间的分隔符。 |
| [getCharactersPerLine()](#getCharactersPerLine--) | 获取文档网格中每行的字符数。 |
| [get班级()](#get班级--) |  |
| [getDifferentFirstPageHeaderFooter()](#getDifferentFirstPageHeaderFooter--) | **True**如果在第一页上使用了不同的页眉或页脚。 |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int-) |  |
| [getEndnoteOptions()](#getEndnoteOptions--) | 提供控制本节中尾注编号和定位的选项。 |
| [getFirstPageTray()](#getFirstPageTray--) | 获取用于部分第一页的纸盘（纸盒）。 |
| [getFooterDistance()](#getFooterDistance--) | 获取页脚和页面底部之间的距离（以磅为单位）。 |
| [getFootnoteOptions()](#getFootnoteOptions--) | 提供控制本节中脚注的编号和位置的选项。 |
| [getGutter()](#getGutter--) | 获取添加到文档装订边距的额外空间量。 |
| [getHeaderDistance()](#getHeaderDistance--) | 获取页眉和页面顶部之间的距离（以磅为单位）。 |
| [getHeadingLevelForChapter()](#getHeadingLevelForChapter--) | 获取应用于文档中章节标题的标题级别样式。 |
| [getLayoutMode()](#getLayoutMode--) | 获取此部分的布局模式。 |
| [getLeftMargin()](#getLeftMargin--) | 获取页面左边缘和正文左边界之间的距离（以磅为单位）。 |
| [getLineNumberCountBy()](#getLineNumberCountBy--) | 获取行号的数字增量。 |
| [getLineNumberDistanceFromText()](#getLineNumberDistanceFromText--) | 获取行号右边缘与文档左边缘之间的距离。 |
| [getLineNumberRestartMode()](#getLineNumberRestartMode--) | 获取行编号的运行方式，即它是在新页面或部分的开头重新开始还是连续运行。 |
| [getLineStartingNumber()](#getLineStartingNumber--) | 获取起始行号。 |
| [getLinesPerPage()](#getLinesPerPage--) | 获取文档网格中每页的行数。 |
| [getMultiplePages()](#getMultiplePages--) | 对于多页文档，获取或设置文档的打印或呈现方式，以便可以将其装订为小册子。 |
| [getOddAndEvenPagesHeaderFooter()](#getOddAndEvenPagesHeaderFooter--) | **True**如果文档对于奇数页和偶数页有不同的页眉和页脚。 |
| [getOrientation()](#getOrientation--) | 获取页面的方向。 |
| [getOtherPagesTray()](#getOtherPagesTray--) | 获取要用于除第一页以外的所有部分的纸盒（纸盒）。 |
| [getPageHeight()](#getPageHeight--) | 获取页面的高度（以磅为单位）。 |
| [getPageNumberStyle()](#getPageNumberStyle--) | 获取页码格式。 |
| [getPageStartingNumber()](#getPageStartingNumber--) | 获取节的起始页码。 |
| [getPageWidth()](#getPageWidth--) | 获取页面的宽度（以磅为单位）。 |
| [getPaperSize()](#getPaperSize--) | 获取纸张大小。 |
| [getRestartPageNumbering()](#getRestartPageNumbering--) | **True**如果页码在节的开头重新开始。 |
| [getRightMargin()](#getRightMargin--) | 获取页面右边缘与正文右边界之间的距离（以磅为单位）。 |
| [getRtlGutter()](#getRtlGutter--) | 获取 Microsoft Word 是否基于从右到左的语言或从左到右的语言为部分使用装订线。 |
| [getSectionStart()](#getSectionStart--) | 获取指定对象的分节符类型。 |
| [getSheetsPerBooklet()](#getSheetsPerBooklet--) | 获取要包含在每个小册子中的页数。 |
| [getSuppressEndnotes()](#getSuppressEndnotes--) | **True**如果尾注打印在下一部分的末尾，它不会抑制尾注。 |
| [getTextColumns()](#getTextColumns--) | 返回一个表示文本列集的集合。 |
| [getTextOrientation()](#getTextOrientation--) | 允许指定[getTextOrientation()](../../com.aspose.words/pagesetup\#getTextOrientation--) / [setTextOrientation(int)](../../com.aspose.words/pagesetup\#setTextOrientation-int-)对于整个页面。 |
| [getTopMargin()](#getTopMargin--) | 获取页面上边缘与正文上边界之间的距离（以磅为单位）。 |
| [getVerticalAlignment()](#getVerticalAlignment--) | 获取文档或节中每一页上文本的垂直对齐方式。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setBidi(boolean value)](#setBidi-boolean-) | 指定此部分包含双向（复杂脚本）文本。 |
| [setBorderAlwaysInFront(boolean value)](#setBorderAlwaysInFront-boolean-) | 指定页面边框相对于相交文本和对象的位置。 |
| [setBorderAppliesTo(int value)](#setBorderAppliesTo-int-) | 指定打印页面边框的页面。 |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object-) |  |
| [setBorderDistanceFrom(int value)](#setBorderDistanceFrom-int-) | 设置一个值，该值指示指定的页面边框是从页面边缘还是从其周围的文本测量的。 |
| [setBorderSurroundsFooter(boolean value)](#setBorderSurroundsFooter-boolean-) | 指定页面边框是包括还是不包括页脚。 |
| [setBorderSurroundsHeader(boolean value)](#setBorderSurroundsHeader-boolean-) | 指定页面边框是包括还是不包括页眉。 |
| [setBottomMargin(double value)](#setBottomMargin-double-) | 设置页面底部边缘和正文底部边界之间的距离（以磅为单位）。 |
| [setChapterPageSeparator(int value)](#setChapterPageSeparator-int-) | 设置出现在章节号和页码之间的分隔符。 |
| [setCharactersPerLine(int value)](#setCharactersPerLine-int-) | 设置文档网格中每行的字符数。 |
| [setDifferentFirstPageHeaderFooter(boolean value)](#setDifferentFirstPageHeaderFooter-boolean-) | **True**如果在第一页上使用了不同的页眉或页脚。 |
| [setFirstPageTray(int value)](#setFirstPageTray-int-) | 设置用于部分第一页的纸盘（纸盒）。 |
| [setFooterDistance(double value)](#setFooterDistance-double-) | 设置页脚和页面底部之间的距离（以磅为单位）。 |
| [setGutter(double value)](#setGutter-double-) | 设置添加到文档装订边距的额外空间量。 |
| [setHeaderDistance(double value)](#setHeaderDistance-double-) | 设置页眉和页面顶部之间的距离（以磅为单位）。 |
| [setHeadingLevelForChapter(int value)](#setHeadingLevelForChapter-int-) | 设置应用于文档中章节标题的标题级别样式。 |
| [setLayoutMode(int value)](#setLayoutMode-int-) | 设置此部分的布局模式。 |
| [setLeftMargin(double value)](#setLeftMargin-double-) | 设置页面左边缘和正文左边界之间的距离（以磅为单位）。 |
| [setLineNumberCountBy(int value)](#setLineNumberCountBy-int-) | 设置行号的数字增量。 |
| [setLineNumberDistanceFromText(double value)](#setLineNumberDistanceFromText-double-) | 设置行号右边缘和文档左边缘之间的距离。 |
| [setLineNumberRestartMode(int value)](#setLineNumberRestartMode-int-) | 设置行编号的运行方式，即是在新页面或部分的开头重新开始还是连续运行。 |
| [setLineStartingNumber(int value)](#setLineStartingNumber-int-) | 设置起始行号。 |
| [setLinesPerPage(int value)](#setLinesPerPage-int-) | 设置文档网格中每页的行数。 |
| [setMultiplePages(int value)](#setMultiplePages-int-) | 对于多页文档，获取或设置文档的打印或呈现方式，以便可以将其装订为小册子。 |
| [setOddAndEvenPagesHeaderFooter(boolean value)](#setOddAndEvenPagesHeaderFooter-boolean-) | **True**如果文档对于奇数页和偶数页有不同的页眉和页脚。 |
| [setOrientation(int value)](#setOrientation-int-) | 设置页面的方向。 |
| [setOtherPagesTray(int value)](#setOtherPagesTray-int-) | 设置要用于除第一页以外的所有部分的纸盘（纸盒）。 |
| [setPageHeight(double value)](#setPageHeight-double-) | 以磅为单位设置页面的高度。 |
| [setPageNumberStyle(int value)](#setPageNumberStyle-int-) | 设置页码格式。 |
| [setPageStartingNumber(int value)](#setPageStartingNumber-int-) | 设置节的起始页码。 |
| [setPageWidth(double value)](#setPageWidth-double-) | 以磅为单位设置页面的宽度。 |
| [setPaperSize(int value)](#setPaperSize-int-) | 设置纸张尺寸。 |
| [setRestartPageNumbering(boolean value)](#setRestartPageNumbering-boolean-) | **True**如果页码在节的开头重新开始。 |
| [setRightMargin(double value)](#setRightMargin-double-) | 设置页面右边缘和正文右边界之间的距离（以磅为单位）。 |
| [setRtlGutter(boolean value)](#setRtlGutter-boolean-) | 设置 Microsoft Word 是根据从右到左的语言还是从左到右的语言为部分使用装订线。 |
| [setSectionStart(int value)](#setSectionStart-int-) | 设置指定对象的分节符类型。 |
| [setSheetsPerBooklet(int value)](#setSheetsPerBooklet-int-) | 设置要包含在每个小册子中的页数。 |
| [setSuppressEndnotes(boolean value)](#setSuppressEndnotes-boolean-) | **True**如果尾注打印在下一部分的末尾，它不会抑制尾注。 |
| [setTextOrientation(int value)](#setTextOrientation-int-) | 允许指定[getTextOrientation()](../../com.aspose.words/pagesetup\#getTextOrientation--) / [setTextOrientation(int)](../../com.aspose.words/pagesetup\#setTextOrientation-int-)对于整个页面。 |
| [setTopMargin(double value)](#setTopMargin-double-) | 设置页面上边缘和正文上边界之间的距离（以磅为单位）。 |
| [setVerticalAlignment(int value)](#setVerticalAlignment-int-) | 设置文档或部分中每一页上文本的垂直对齐方式。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### clearFormatting() {#clearFormatting--}
```
public void clearFormatting()
```


将页面设置重置为默认纸张尺寸、边距和方向。

### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**退货:**
布尔值
### fetchInheritedBorderAttr(int key) {#fetchInheritedBorderAttr-int-}
```
public Object fetchInheritedBorderAttr(int key)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货:**
java.lang.Object
### getBidi() {#getBidi--}
```
public boolean getBidi()
```


指定此部分包含双向（复杂脚本）文本。

如果为 true，则此部分中的列从右到左排列。

**退货:**
boolean - 对应的布尔值。
### getBorderAlwaysInFront() {#getBorderAlwaysInFront--}
```
public boolean getBorderAlwaysInFront()
```


指定页面边框相对于相交文本和对象的位置。

**退货:**
boolean - 对应的布尔值。
### getBorderAppliesTo() {#getBorderAppliesTo--}
```
public int getBorderAppliesTo()
```


指定打印页面边框的页面。

**退货:**
int - 对应的 int 值。返回值是以下之一[PageBorderAppliesTo](../../com.aspose.words/pageborderappliesto)常数。
### getBorderDistanceFrom() {#getBorderDistanceFrom--}
```
public int getBorderDistanceFrom()
```


获取一个值，该值指示指定的页面边框是从页面边缘还是从其周围的文本测量的。

**退货:**
 int - 一个值，指示指定的页面边框是从页面边缘还是从它周围的文本测量的。返回值是以下之一[PageBorderDistanceFrom](../../com.aspose.words/pageborderdistancefrom)常数。
### getBorderSurroundsFooter() {#getBorderSurroundsFooter--}
```
public boolean getBorderSurroundsFooter()
```


指定页面边框是包括还是不包括页脚。请注意，更改此属性会影响文档中的所有部分。

**退货:**
boolean - 对应的布尔值。
### getBorderSurroundsHeader() {#getBorderSurroundsHeader--}
```
public boolean getBorderSurroundsHeader()
```


指定页面边框是包括还是不包括页眉。请注意，更改此属性会影响文档中的所有部分。

**退货:**
boolean - 对应的布尔值。
### getBorders() {#getBorders--}
```
public BorderCollection getBorders()
```


获取页面边框的集合。

**退货:**
[BorderCollection](../../com.aspose.words/bordercollection) - 页面边框的集合。
### getBottomMargin() {#getBottomMargin--}
```
public double getBottomMargin()
```


获取页面底部边缘和正文底部边界之间的距离（以磅为单位）。

**退货:**
double - 页面底部边缘和正文底部边界之间的距离（以磅为单位）。
### getChapterPageSeparator() {#getChapterPageSeparator--}
```
public int getChapterPageSeparator()
```


获取出现在章节号和页码之间的分隔符。

在创建包含章节编号的页码之前，文档标题必须应用编号大纲格式。

**退货:**
 int - 出现在章节号和页码之间的分隔符。返回值是以下之一[ChapterPageSeparator](../../com.aspose.words/chapterpageseparator)常数。
### getCharactersPerLine() {#getCharactersPerLine--}
```
public int getCharactersPerLine()
```


获取文档网格中每行的字符数。

该属性的最小值为 1。最大值取决于 Normal 样式的页面宽度和字体大小。最小字符间距为字体大小的 90%。例如，一英寸页边距的 Letter 页面每行的最大字符数为 43。

默认情况下，该属性有一个值，其字符间距等于 Normal 样式的字体大小。

**退货:**
int - 文档网格中每行的字符数。
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getDifferentFirstPageHeaderFooter() {#getDifferentFirstPageHeaderFooter--}
```
public boolean getDifferentFirstPageHeaderFooter()
```


**True**如果在第一页上使用了不同的页眉或页脚。

**退货:**
boolean - 对应的布尔值。
### getDirectBorderAttr(int key) {#getDirectBorderAttr-int-}
```
public Object getDirectBorderAttr(int key)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货:**
java.lang.Object
### getEndnoteOptions() {#getEndnoteOptions--}
```
public EndnoteOptions getEndnoteOptions()
```


提供控制本节中尾注编号和定位的选项。

**退货:**
[EndnoteOptions](../../com.aspose.words/endnoteoptions) - 相应的[EndnoteOptions](../../com.aspose.words/endnoteoptions)价值。
### getFirstPageTray() {#getFirstPageTray--}
```
public int getFirstPageTray()
```


获取用于部分第一页的纸盘（纸盒）。该值是特定于实现（打印机）的。

**退货:**
int - 用于部分第一页的纸盒（纸盒）。
### getFooterDistance() {#getFooterDistance--}
```
public double getFooterDistance()
```


获取页脚和页面底部之间的距离（以磅为单位）。

**退货:**
double - 页脚和页面底部之间的距离（以磅为单位）。
### getFootnoteOptions() {#getFootnoteOptions--}
```
public FootnoteOptions getFootnoteOptions()
```


提供控制本节中脚注的编号和位置的选项。

**退货:**
[FootnoteOptions](../../com.aspose.words/footnoteoptions) - 相应的[FootnoteOptions](../../com.aspose.words/footnoteoptions)价值。
### getGutter() {#getGutter--}
```
public double getGutter()
```


获取添加到文档装订边距的额外空间量。

**退货:**
double - 添加到文档装订边距的额外空间量。
### getHeaderDistance() {#getHeaderDistance--}
```
public double getHeaderDistance()
```


获取页眉和页面顶部之间的距离（以磅为单位）。

**退货:**
double - 页眉和页面顶部之间的距离（以磅为单位）。
### getHeadingLevelForChapter() {#getHeadingLevelForChapter--}
```
public int getHeadingLevelForChapter()
```


获取应用于文档中章节标题的标题级别样式。

可以是从 0 到 9 的数字。如果应用于页码，0 表示没有章节编号。

在创建包含章节编号的页码之前，文档标题必须应用编号大纲格式。

**退货:**
int - 应用于文档中章节标题的标题级别样式。
### getLayoutMode() {#getLayoutMode--}
```
public int getLayoutMode()
```


获取此部分的布局模式。

**退货:**
 int - 本节的布局模式。返回值是以下之一[SectionLayoutMode](../../com.aspose.words/sectionlayoutmode)常数。
### getLeftMargin() {#getLeftMargin--}
```
public double getLeftMargin()
```


获取页面左边缘和正文左边界之间的距离（以磅为单位）。

**退货:**
double - 页面左边缘与正文左边界之间的距离（以磅为单位）。
### getLineNumberCountBy() {#getLineNumberCountBy--}
```
public int getLineNumberCountBy()
```


获取行号的数字增量。

**退货:**
int - 行号的数字增量。
### getLineNumberDistanceFromText() {#getLineNumberDistanceFromText--}
```
public double getLineNumberDistanceFromText()
```


获取行号右边缘与文档左边缘之间的距离。将此属性设置为零以实现行号和文档文本之间的自动距离。

**退货:**
double - 行号右边缘与文档左边缘之间的距离。
### getLineNumberRestartMode() {#getLineNumberRestartMode--}
```
public int getLineNumberRestartMode()
```


获取行编号的运行方式，即它是在新页面或部分的开头重新开始还是连续运行。

**退货:**
 int - 行号的运行方式，即它是在新页面或部分的开头重新开始还是连续运行。返回值是以下之一[LineNumberRestartMode](../../com.aspose.words/linenumberrestartmode)常数。
### getLineStartingNumber() {#getLineStartingNumber--}
```
public int getLineStartingNumber()
```


获取起始行号。

**退货:**
int - 起始行号。
### getLinesPerPage() {#getLinesPerPage--}
```
public int getLinesPerPage()
```


获取文档网格中每页的行数。

该属性的最小值为 1。最大值取决于 Normal 样式的页面高度和字体大小。最小行距是字体大小的 136%。例如，每页边距为 1 英寸的 Letter 页面的最大行数为 39。

默认情况下，该属性有一个值，在该值上，行距是 Normal 样式字体大小的 1.5 倍。

**退货:**
int - 文档网格中每页的行数。
### getMultiplePages() {#getMultiplePages--}
```
public int getMultiplePages()
```


对于多页文档，获取或设置文档的打印或呈现方式，以便可以将其装订为小册子。

**退货:**
int - 对应的 int 值。返回值是以下之一[MultiplePages类型](../../com.aspose.words/multiplepagestype)常数。
### getOddAndEvenPagesHeaderFooter() {#getOddAndEvenPagesHeaderFooter--}
```
public boolean getOddAndEvenPagesHeaderFooter()
```


**True**如果文档对于奇数页和偶数页有不同的页眉和页脚。请注意，更改此属性会影响文档中的所有部分。

**退货:**
boolean - 对应的布尔值。
### getOrientation() {#getOrientation--}
```
public int getOrientation()
```


获取页面的方向。

改变**Orientation**掉期[getPageWidth()](../../com.aspose.words/pagesetup\#getPageWidth--) / [setPageWidth(double)](../../com.aspose.words/pagesetup\#setPageWidth-double-)和[getPageHeight()](../../com.aspose.words/pagesetup\#getPageHeight--) / [setPageHeight(double)](../../com.aspose.words/pagesetup\#setPageHeight-double-).

**退货:**
int - 页面的方向。返回值是以下之一[Orientation](../../com.aspose.words/orientation)常数。
### getOtherPagesTray() {#getOtherPagesTray--}
```
public int getOtherPagesTray()
```


获取要用于除第一页以外的所有部分的纸盒（纸盒）。该值是特定于实现（打印机）的。

**退货:**
int - 用于除第一页以外的所有部分的纸盒（纸盒）。
### getPageHeight() {#getPageHeight--}
```
public double getPageHeight()
```


获取页面的高度（以磅为单位）。

**退货:**
double - 以磅为单位的页面高度。
### getPageNumberStyle() {#getPageNumberStyle--}
```
public int getPageNumberStyle()
```


获取页码格式。

**退货:**
 int - 页码格式。返回值是以下之一[NumberStyle](../../com.aspose.words/numberstyle)常数。
### getPageStartingNumber() {#getPageStartingNumber--}
```
public int getPageStartingNumber()
```


获取节的起始页码。这[getRestartPageNumbering()](../../com.aspose.words/pagesetup\#getRestartPageNumbering--) / [setRestartPageNumbering(boolean)](../../com.aspose.words/pagesetup\#setRestartPageNumbering-boolean-)属性，如果设置为**false** 将覆盖**PageStartingNumber**属性，以便页码可以从上一节继续。

**退货:**
int - 节的起始页码。
### getPageWidth() {#getPageWidth--}
```
public double getPageWidth()
```


获取页面的宽度（以磅为单位）。

**退货:**
double - 以磅为单位的页面宽度。
### getPaperSize() {#getPaperSize--}
```
public int getPaperSize()
```


获取纸张大小。

设置此属性更新[getPageWidth()](../../com.aspose.words/pagesetup\#getPageWidth--) / [setPageWidth(double)](../../com.aspose.words/pagesetup\#setPageWidth-double-)和[getPageHeight()](../../com.aspose.words/pagesetup\#getPageHeight--) / [setPageHeight(double)](../../com.aspose.words/pagesetup\#setPageHeight-double-)价值观。将此值设置为[PaperSize.CUSTOM](../../com.aspose.words/papersize\#CUSTOM)不会更改现有值。

**退货:**
int - 纸张大小。返回值是以下之一[PaperSize](../../com.aspose.words/papersize)常数。
### getRestartPageNumbering() {#getRestartPageNumbering--}
```
public boolean getRestartPageNumbering()
```


**True**如果页码在节的开头重新开始。如果设置为**false**， 这**RestartPageNumbering**属性将覆盖[getPageStartingNumber()](../../com.aspose.words/pagesetup\#getPageStartingNumber--) / [setPageStartingNumber(int)](../../com.aspose.words/pagesetup\#setPageStartingNumber-int-)属性，以便页码可以从上一节继续。

**退货:**
boolean - 对应的布尔值。
### getRightMargin() {#getRightMargin--}
```
public double getRightMargin()
```


获取页面右边缘与正文右边界之间的距离（以磅为单位）。

**退货:**
double - 页面右边缘与正文右边界之间的距离（以磅为单位）。
### getRtlGutter() {#getRtlGutter--}
```
public boolean getRtlGutter()
```


获取 Microsoft Word 是否基于从右到左的语言或从左到右的语言为部分使用装订线。

**退货:**
boolean - Microsoft Word 是否基于从右到左的语言或从左到右的语言为部分使用装订线。
### getSectionStart() {#getSectionStart--}
```
public int getSectionStart()
```


获取指定对象的分节符类型。

**退货:**
 int - 指定对象的分节符类型。返回值是以下之一[SectionStart](../../com.aspose.words/sectionstart)常数。
### getSheetsPerBooklet() {#getSheetsPerBooklet--}
```
public int getSheetsPerBooklet()
```


获取要包含在每个小册子中的页数。

**退货:**
int - 每本小册子要包含的页数。
### getSuppressEndnotes() {#getSuppressEndnotes--}
```
public boolean getSuppressEndnotes()
```


**True**如果尾注打印在下一部分的末尾，它不会抑制尾注。隐藏的尾注打印在该部分的尾注之前。

**退货:**
boolean - 对应的布尔值。
### getTextColumns() {#getTextColumns--}
```
public TextColumnCollection getTextColumns()
```


返回一个表示文本列集的集合。

**退货:**
[TextColumnCollection](../../com.aspose.words/textcolumncollection) - 表示一组文本列的集合。
### getTextOrientation() {#getTextOrientation--}
```
public int getTextOrientation()
```


允许指定[getTextOrientation()](../../com.aspose.words/pagesetup\#getTextOrientation--) / [setTextOrientation(int)](../../com.aspose.words/pagesetup\#setTextOrientation-int-)对于整个页面。默认值为[TextOrientation.HORIZONTAL](../../com.aspose.words/textorientation\#HORIZONTAL)此属性仅支持 MS Word 本机格式 DOCX、WML、RTF 和 DOC。

**退货:**
int - 对应的 int 值。返回值是以下之一[TextOrientation](../../com.aspose.words/textorientation)常数。
### getTopMargin() {#getTopMargin--}
```
public double getTopMargin()
```


获取页面上边缘与正文上边界之间的距离（以磅为单位）。

**退货:**
double - 页面上边缘与正文上边界之间的距离（以磅为单位）。
### getVerticalAlignment() {#getVerticalAlignment--}
```
public int getVerticalAlignment()
```


获取文档或节中每一页上文本的垂直对齐方式。

**退货:**
 int - 文档或部分中每一页上文本的垂直对齐方式。返回值是以下之一[PageVerticalAlignment](../../com.aspose.words/pageverticalalignment)常数。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setBidi(boolean value) {#setBidi-boolean-}
```
public void setBidi(boolean value)
```


指定此部分包含双向（复杂脚本）文本。

如果为 true，则此部分中的列从右到左排列。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setBorderAlwaysInFront(boolean value) {#setBorderAlwaysInFront-boolean-}
```
public void setBorderAlwaysInFront(boolean value)
```


指定页面边框相对于相交文本和对象的位置。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setBorderAppliesTo(int value) {#setBorderAppliesTo-int-}
```
public void setBorderAppliesTo(int value)
```


指定打印页面边框的页面。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[PageBorderAppliesTo](../../com.aspose.words/pageborderappliesto)常数。 |

### setBorderAttr(int key, Object value) {#setBorderAttr-int-java.lang.Object-}
```
public void setBorderAttr(int key, Object value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setBorderDistanceFrom(int value) {#setBorderDistanceFrom-int-}
```
public void setBorderDistanceFrom(int value)
```


设置一个值，该值指示指定的页面边框是从页面边缘还是从其周围的文本测量的。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 一个值，指示指定的页面边框是从页面边缘还是从其周围的文本测量的。该值必须是以下之一[PageBorderDistanceFrom](../../com.aspose.words/pageborderdistancefrom)常数。 |

### setBorderSurroundsFooter(boolean value) {#setBorderSurroundsFooter-boolean-}
```
public void setBorderSurroundsFooter(boolean value)
```


指定页面边框是包括还是不包括页脚。请注意，更改此属性会影响文档中的所有部分。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setBorderSurroundsHeader(boolean value) {#setBorderSurroundsHeader-boolean-}
```
public void setBorderSurroundsHeader(boolean value)
```


指定页面边框是包括还是不包括页眉。请注意，更改此属性会影响文档中的所有部分。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setBottomMargin(double value) {#setBottomMargin-double-}
```
public void setBottomMargin(double value)
```


设置页面底部边缘和正文底部边界之间的距离（以磅为单位）。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 页面底部边缘与正文底部边界之间的距离（以磅为单位）。 |

### setChapterPageSeparator(int value) {#setChapterPageSeparator-int-}
```
public void setChapterPageSeparator(int value)
```


设置出现在章节号和页码之间的分隔符。

在创建包含章节编号的页码之前，文档标题必须应用编号大纲格式。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 出现在章节号和页码之间的分隔符。该值必须是以下之一[ChapterPageSeparator](../../com.aspose.words/chapterpageseparator)常数。 |

### setCharactersPerLine(int value) {#setCharactersPerLine-int-}
```
public void setCharactersPerLine(int value)
```


设置文档网格中每行的字符数。

该属性的最小值为 1。最大值取决于 Normal 样式的页面宽度和字体大小。最小字符间距为字体大小的 90%。例如，一英寸页边距的 Letter 页面每行的最大字符数为 43。

默认情况下，该属性有一个值，其字符间距等于 Normal 样式的字体大小。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 文档网格中每行的字符数。 |

### setDifferentFirstPageHeaderFooter(boolean value) {#setDifferentFirstPageHeaderFooter-boolean-}
```
public void setDifferentFirstPageHeaderFooter(boolean value)
```


**True**如果在第一页上使用了不同的页眉或页脚。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setFirstPageTray(int value) {#setFirstPageTray-int-}
```
public void setFirstPageTray(int value)
```


设置用于部分第一页的纸盘（纸盒）。该值是特定于实现（打印机）的。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 用于部分第一页的纸盒（纸盒）。 |

### setFooterDistance(double value) {#setFooterDistance-double-}
```
public void setFooterDistance(double value)
```


设置页脚和页面底部之间的距离（以磅为单位）。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 页脚和页面底部之间的距离（以磅为单位）。 |

### setGutter(double value) {#setGutter-double-}
```
public void setGutter(double value)
```


设置添加到文档装订边距的额外空间量。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 添加到文档装订边距的额外空间量。 |

### setHeaderDistance(double value) {#setHeaderDistance-double-}
```
public void setHeaderDistance(double value)
```


设置页眉和页面顶部之间的距离（以磅为单位）。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 页眉和页面顶部之间的距离（以磅为单位）。 |

### setHeadingLevelForChapter(int value) {#setHeadingLevelForChapter-int-}
```
public void setHeadingLevelForChapter(int value)
```


设置应用于文档中章节标题的标题级别样式。

可以是从 0 到 9 的数字。如果应用于页码，0 表示没有章节编号。

在创建包含章节编号的页码之前，文档标题必须应用编号大纲格式。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 应用于文档中章节标题的标题级别样式。 |

### setLayoutMode(int value) {#setLayoutMode-int-}
```
public void setLayoutMode(int value)
```


设置此部分的布局模式。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 本节的布局模式。该值必须是以下之一[SectionLayoutMode](../../com.aspose.words/sectionlayoutmode)常数。 |

### setLeftMargin(double value) {#setLeftMargin-double-}
```
public void setLeftMargin(double value)
```


设置页面左边缘和正文左边界之间的距离（以磅为单位）。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 页面左边缘与正文左边界之间的距离（以磅为单位）。 |

### setLineNumberCountBy(int value) {#setLineNumberCountBy-int-}
```
public void setLineNumberCountBy(int value)
```


设置行号的数字增量。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 行号的数字增量。 |

### setLineNumberDistanceFromText(double value) {#setLineNumberDistanceFromText-double-}
```
public void setLineNumberDistanceFromText(double value)
```


设置行号右边缘和文档左边缘之间的距离。将此属性设置为零以实现行号和文档文本之间的自动距离。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 行号右边缘与文档左边缘之间的距离。 |

### setLineNumberRestartMode(int value) {#setLineNumberRestartMode-int-}
```
public void setLineNumberRestartMode(int value)
```


设置行编号的运行方式，即是在新页面或部分的开头重新开始还是连续运行。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 行编号的运行方式是，它是在新页面或部分的开头重新开始还是连续运行。该值必须是以下之一[LineNumberRestartMode](../../com.aspose.words/linenumberrestartmode)常数。 |

### setLineStartingNumber(int value) {#setLineStartingNumber-int-}
```
public void setLineStartingNumber(int value)
```


设置起始行号。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 起始行号。 |

### setLinesPerPage(int value) {#setLinesPerPage-int-}
```
public void setLinesPerPage(int value)
```


设置文档网格中每页的行数。

该属性的最小值为 1。最大值取决于 Normal 样式的页面高度和字体大小。最小行距是字体大小的 136%。例如，每页边距为 1 英寸的 Letter 页面的最大行数为 39。

默认情况下，该属性有一个值，在该值上，行距是 Normal 样式字体大小的 1.5 倍。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 文档网格中每页的行数。 |

### setMultiplePages(int value) {#setMultiplePages-int-}
```
public void setMultiplePages(int value)
```


对于多页文档，获取或设置文档的打印或呈现方式，以便可以将其装订为小册子。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[MultiplePages类型](../../com.aspose.words/multiplepagestype)常数。 |

### setOddAndEvenPagesHeaderFooter(boolean value) {#setOddAndEvenPagesHeaderFooter-boolean-}
```
public void setOddAndEvenPagesHeaderFooter(boolean value)
```


**True**如果文档对于奇数页和偶数页有不同的页眉和页脚。请注意，更改此属性会影响文档中的所有部分。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setOrientation(int value) {#setOrientation-int-}
```
public void setOrientation(int value)
```


设置页面的方向。

改变**Orientation**掉期[getPageWidth()](../../com.aspose.words/pagesetup\#getPageWidth--) / [setPageWidth(double)](../../com.aspose.words/pagesetup\#setPageWidth-double-)和[getPageHeight()](../../com.aspose.words/pagesetup\#getPageHeight--) / [setPageHeight(double)](../../com.aspose.words/pagesetup\#setPageHeight-double-).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 页面的方向。该值必须是以下之一[Orientation](../../com.aspose.words/orientation)常数。 |

### setOtherPagesTray(int value) {#setOtherPagesTray-int-}
```
public void setOtherPagesTray(int value)
```


设置要用于除第一页以外的所有部分的纸盘（纸盒）。该值是特定于实现（打印机）的。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 用于除第一页以外的所有部分的纸盘（纸盒）。 |

### setPageHeight(double value) {#setPageHeight-double-}
```
public void setPageHeight(double value)
```


以磅为单位设置页面的高度。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 以磅为单位的页面高度。 |

### setPageNumberStyle(int value) {#setPageNumberStyle-int-}
```
public void setPageNumberStyle(int value)
```


设置页码格式。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 页码格式。该值必须是以下之一[NumberStyle](../../com.aspose.words/numberstyle)常数。 |

### setPageStartingNumber(int value) {#setPageStartingNumber-int-}
```
public void setPageStartingNumber(int value)
```


设置节的起始页码。这[getRestartPageNumbering()](../../com.aspose.words/pagesetup\#getRestartPageNumbering--) / [setRestartPageNumbering(boolean)](../../com.aspose.words/pagesetup\#setRestartPageNumbering-boolean-)属性，如果设置为**false** 将覆盖**PageStartingNumber**属性，以便页码可以从上一节继续。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 节的起始页码。 |

### setPageWidth(double value) {#setPageWidth-double-}
```
public void setPageWidth(double value)
```


以磅为单位设置页面的宽度。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 以磅为单位的页面宽度。 |

### setPaperSize(int value) {#setPaperSize-int-}
```
public void setPaperSize(int value)
```


设置纸张尺寸。

设置此属性更新[getPageWidth()](../../com.aspose.words/pagesetup\#getPageWidth--) / [setPageWidth(double)](../../com.aspose.words/pagesetup\#setPageWidth-double-)和[getPageHeight()](../../com.aspose.words/pagesetup\#getPageHeight--) / [setPageHeight(double)](../../com.aspose.words/pagesetup\#setPageHeight-double-)价值观。将此值设置为[PaperSize.CUSTOM](../../com.aspose.words/papersize\#CUSTOM)不会更改现有值。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 纸张大小。该值必须是以下之一[PaperSize](../../com.aspose.words/papersize)常数。 |

### setRestartPageNumbering(boolean value) {#setRestartPageNumbering-boolean-}
```
public void setRestartPageNumbering(boolean value)
```


**True**如果页码在节的开头重新开始。如果设置为**false**， 这**RestartPageNumbering**属性将覆盖[getPageStartingNumber()](../../com.aspose.words/pagesetup\#getPageStartingNumber--) / [setPageStartingNumber(int)](../../com.aspose.words/pagesetup\#setPageStartingNumber-int-)属性，以便页码可以从上一节继续。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setRightMargin(double value) {#setRightMargin-double-}
```
public void setRightMargin(double value)
```


设置页面右边缘和正文右边界之间的距离（以磅为单位）。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 页面右边缘与正文右边界之间的距离（以磅为单位）。 |

### setRtlGutter(boolean value) {#setRtlGutter-boolean-}
```
public void setRtlGutter(boolean value)
```


设置 Microsoft Word 是根据从右到左的语言还是从左到右的语言为部分使用装订线。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | Microsoft Word 是否基于从右到左的语言或从左到右的语言为该部分使用装订线。 |

### setSectionStart(int value) {#setSectionStart-int-}
```
public void setSectionStart(int value)
```


设置指定对象的分节符类型。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 指定对象的分节符类型。该值必须是以下之一[SectionStart](../../com.aspose.words/sectionstart)常数。 |

### setSheetsPerBooklet(int value) {#setSheetsPerBooklet-int-}
```
public void setSheetsPerBooklet(int value)
```


设置要包含在每个小册子中的页数。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 每本小册子要包含的页数。 |

### setSuppressEndnotes(boolean value) {#setSuppressEndnotes-boolean-}
```
public void setSuppressEndnotes(boolean value)
```


**True**如果尾注打印在下一部分的末尾，它不会抑制尾注。隐藏的尾注打印在该部分的尾注之前。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setTextOrientation(int value) {#setTextOrientation-int-}
```
public void setTextOrientation(int value)
```


允许指定[getTextOrientation()](../../com.aspose.words/pagesetup\#getTextOrientation--) / [setTextOrientation(int)](../../com.aspose.words/pagesetup\#setTextOrientation-int-)对于整个页面。默认值为[TextOrientation.HORIZONTAL](../../com.aspose.words/textorientation\#HORIZONTAL)此属性仅支持 MS Word 本机格式 DOCX、WML、RTF 和 DOC。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[TextOrientation](../../com.aspose.words/textorientation)常数。 |

### setTopMargin(double value) {#setTopMargin-double-}
```
public void setTopMargin(double value)
```


设置页面上边缘和正文上边界之间的距离（以磅为单位）。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 页面上边缘与正文上边界之间的距离（以磅为单位）。 |

### setVerticalAlignment(int value) {#setVerticalAlignment-int-}
```
public void setVerticalAlignment(int value)
```


设置文档或部分中每一页上文本的垂直对齐方式。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 文档或部分中每一页上文本的垂直对齐方式。该值必须是以下之一[PageVerticalAlignment](../../com.aspose.words/pageverticalalignment)常数。 |

### toString() {#toString--}
```
public String toString()
```




**退货:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
