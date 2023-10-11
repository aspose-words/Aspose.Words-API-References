---
title: Class DocumentBuilder
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.DocumentBuilder 班级. 提供插入文本图像和其他内容指定字体段落和部分格式的方法
type: docs
weight: 450
url: /zh/net/aspose.words/documentbuilder/
---
## DocumentBuilder class

提供插入文本、图像和其他内容、指定字体、段落和部分格式的方法。

要了解更多信息，请访问[文档生成器概述](https://docs.aspose.com/words/net/document-builder-overview/)文档文章。

```csharp
public class DocumentBuilder
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [DocumentBuilder](documentbuilder/#constructor)() | 初始化此类的新实例。 |
| [DocumentBuilder](documentbuilder/#constructor_1)(Document) | 初始化此类的新实例。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Bold](../../aspose.words/documentbuilder/bold/) { get; set; } | 如果字体格式为粗体，则为 True。 |
| [CellFormat](../../aspose.words/documentbuilder/cellformat/) { get; } | 返回表示当前表格单元格格式属性的对象。 |
| [CurrentNode](../../aspose.words/documentbuilder/currentnode/) { get; } | 获取当前在此 DocumentBuilder 中选择的节点。 |
| [CurrentParagraph](../../aspose.words/documentbuilder/currentparagraph/) { get; } | 获取当前选中的段落`DocumentBuilder`. |
| [CurrentSection](../../aspose.words/documentbuilder/currentsection/) { get; } | 获取当前在此选择的部分`DocumentBuilder`. |
| [CurrentStory](../../aspose.words/documentbuilder/currentstory/) { get; } | 获取当前在此选择的故事`DocumentBuilder`. |
| [CurrentStructuredDocumentTag](../../aspose.words/documentbuilder/currentstructureddocumenttag/) { get; } | 获取当前在此选择的结构化文档标签`DocumentBuilder`. |
| [Document](../../aspose.words/documentbuilder/document/) { get; set; } | 获取或设置[`Document`](./document/)该对象附加到的对象。 |
| [Font](../../aspose.words/documentbuilder/font/) { get; } | 返回表示当前字体格式属性的对象。 |
| [IsAtEndOfParagraph](../../aspose.words/documentbuilder/isatendofparagraph/) { get; } | 返回`真的`如果光标位于当前段落的末尾。 |
| [IsAtEndOfStructuredDocumentTag](../../aspose.words/documentbuilder/isatendofstructureddocumenttag/) { get; } | 返回 **真的**如果光标位于结构化文档标记的末尾。 |
| [IsAtStartOfParagraph](../../aspose.words/documentbuilder/isatstartofparagraph/) { get; } | 返回`真的`如果光标位于当前段落的开头（光标之前没有文本）。 |
| [Italic](../../aspose.words/documentbuilder/italic/) { get; set; } | 如果字体格式为斜体，则为 True。 |
| [ListFormat](../../aspose.words/documentbuilder/listformat/) { get; } | 返回一个表示当前列表格式属性的对象。 |
| [PageSetup](../../aspose.words/documentbuilder/pagesetup/) { get; } | 返回一个表示当前页面设置和节属性的对象。 |
| [ParagraphFormat](../../aspose.words/documentbuilder/paragraphformat/) { get; } | 返回一个表示当前段落格式属性的对象。 |
| [RowFormat](../../aspose.words/documentbuilder/rowformat/) { get; } | 返回一个表示当前表行格式属性的对象。 |
| [Underline](../../aspose.words/documentbuilder/underline/) { get; set; } | 获取/设置当前字体的下划线类型。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [DeleteRow](../../aspose.words/documentbuilder/deleterow/)(int, int) | 从表中删除一行。 |
| [EndBookmark](../../aspose.words/documentbuilder/endbookmark/)(string) | 将文档中的当前位置标记为书签结束。 |
| [EndColumnBookmark](../../aspose.words/documentbuilder/endcolumnbookmark/)(string) | 将文档中的当前位置标记为列书签末尾。该位置必须位于表格单元格中。 |
| [EndEditableRange](../../aspose.words/documentbuilder/endeditablerange/#endeditablerange)() | 将文档中的当前位置标记为可编辑范围结束。 |
| [EndEditableRange](../../aspose.words/documentbuilder/endeditablerange/#endeditablerange_1)(EditableRangeStart) | 将文档中的当前位置标记为可编辑范围结束。 |
| [EndRow](../../aspose.words/documentbuilder/endrow/)() | 结束文档中的表格行。 |
| [EndTable](../../aspose.words/documentbuilder/endtable/)() | 结束文档中的表格。 |
| [InsertBreak](../../aspose.words/documentbuilder/insertbreak/)(BreakType) | 将指定类型的中断插入到文档中。 |
| [InsertCell](../../aspose.words/documentbuilder/insertcell/)() | 将表格单元格插入文档中。 |
| [InsertChart](../../aspose.words/documentbuilder/insertchart/#insertchart_1)(ChartType, double, double) | 将图表对象插入到文档中并将其缩放至指定大小。 |
| [InsertChart](../../aspose.words/documentbuilder/insertchart/#insertchart)(ChartType, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | 将图表对象插入到文档中并将其缩放至指定大小。 |
| [InsertCheckBox](../../aspose.words/documentbuilder/insertcheckbox/#insertcheckbox_1)(string, bool, int) | 在当前位置插入复选框表单字段。 |
| [InsertCheckBox](../../aspose.words/documentbuilder/insertcheckbox/#insertcheckbox)(string, bool, bool, int) | 在当前位置插入复选框表单字段。 |
| [InsertComboBox](../../aspose.words/documentbuilder/insertcombobox/)(string, string[], int) | 在当前位置插入组合框表单字段。 |
| [InsertDocument](../../aspose.words/documentbuilder/insertdocument/#insertdocument)(Document, ImportFormatMode) | 在光标位置插入文档。 |
| [InsertDocument](../../aspose.words/documentbuilder/insertdocument/#insertdocument_1)(Document, ImportFormatMode, ImportFormatOptions) | 在光标位置插入文档。 |
| [InsertDocumentInline](../../aspose.words/documentbuilder/insertdocumentinline/)(Document, ImportFormatMode, ImportFormatOptions) |  |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield_1)(string) | 将 Word 字段插入文档并更新字段结果。 |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield)(FieldType, bool) | 将 Word 字段插入文档并可选择更新字段结果。 |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield_2)(string, string) | 将 Word 字段插入到文档中，而不更新字段结果。 |
| [InsertFootnote](../../aspose.words/documentbuilder/insertfootnote/#insertfootnote)(FootnoteType, string) | 在文档中插入脚注或尾注。 |
| [InsertFootnote](../../aspose.words/documentbuilder/insertfootnote/#insertfootnote_1)(FootnoteType, string, string) | 在文档中插入脚注或尾注。 |
| [InsertHorizontalRule](../../aspose.words/documentbuilder/inserthorizontalrule/)() | 将水平标尺形状插入文档中。 |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml)(string) | 将 HTML 字符串插入文档中。 |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml_2)(string, bool) | 将 HTML 字符串插入文档中。 |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml_1)(string, HtmlInsertOptions) | 将 HTML 字符串插入到文档中。允许指定附加选项。 |
| [InsertHyperlink](../../aspose.words/documentbuilder/inserthyperlink/)(string, string, bool) | 将超链接插入到文档中。 |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage)(byte[]) | 将字节数组中的图像插入到文档中。图像以 100% 比例内嵌插入。 |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_3)(Image) | 插入来自 .NET 的图像Image 对象放入文档中。图像以 100% 比例内嵌插入。 |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_6)(Stream) | 将图像从流插入到文档中。图像以 100% 比例内嵌插入。 |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_9)(string) | 将文件或 URL 中的图像插入到文档中。图像以 100% 比例内嵌插入。 |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_2)(byte[], double, double) | 将字节数组中的内联图像插入到文档中并将其缩放到指定的大小。 |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_5)(Image, double, double) | 从 .NET 插入内嵌图像Image 对象放入文档中并将其缩放至指定大小。 |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_8)(Stream, double, double) | 将内嵌图像从流插入到文档中并将其缩放到指定的大小。 |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_11)(string, double, double) | 将文件或 URL 中的内嵌图像插入到文档中，并将其缩放到指定的大小。 |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_1)(byte[], RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | 在指定位置和大小处插入字节数组中的图像。 |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_4)(Image, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | 插入来自 .NET 的图像Image 指定位置和大小的对象。 |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_7)(Stream, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | 在指定位置和大小处插入流中的图像。 |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_10)(string, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | 在指定位置和大小插入文件或 URL 中的图像。 |
| [InsertNode](../../aspose.words/documentbuilder/insertnode/)(Node) | 在光标前插入一个节点。 |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject)(Stream, string, bool, Stream) | 将嵌入的 OLE 对象从流插入到文档中。 |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject_1)(string, bool, bool, Stream) | 将嵌入或链接的 OLE 对象从文件插入到文档中。使用文件扩展名检测 OLE 对象类型。 |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject_2)(string, string, bool, bool, Stream) | 将嵌入或链接的 OLE 对象从文件插入到文档中。使用给定的 progID 参数检测 OLE 对象类型。 |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon)(Stream, string, string, string) | 将嵌入的 OLE 对象作为图标从流插入到文档中。 允许指定图标文件和标题。使用给定的 progID 参数检测 OLE 对象类型。 |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon_1)(string, bool, string, string) | 将嵌入或链接的 OLE 对象作为图标插入到文档中。 允许指定图标文件和标题。使用文件扩展名检测 OLE 对象类型。 |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon_2)(string, string, bool, string, string) | 将嵌入或链接的 OLE 对象作为图标插入到文档中。 允许指定图标文件和标题。使用给定的 progID 参数检测 OLE 对象类型。 |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_1)(string, double, double) | 将在线视频对象插入到文档中并将其缩放到指定的大小。 |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_3)(string, string, byte[], double, double) | 将在线视频对象插入到文档中并将其缩放到指定的大小。 |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo)(string, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | 将在线视频对象插入到文档中并将其缩放到指定的大小。 |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_2)(string, string, byte[], RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | 将在线视频对象插入到文档中并将其缩放到指定的大小。 |
| [InsertParagraph](../../aspose.words/documentbuilder/insertparagraph/)() | 在文档中插入段落分隔符。 |
| [InsertShape](../../aspose.words/documentbuilder/insertshape/#insertshape_1)(ShapeType, double, double) | 插入指定类型和大小的内联形状。 |
| [InsertShape](../../aspose.words/documentbuilder/insertshape/#insertshape)(ShapeType, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | 插入具有指定位置、大小和文本换行类型的自由浮动形状。 |
| [InsertSignatureLine](../../aspose.words/documentbuilder/insertsignatureline/#insertsignatureline)(SignatureLineOptions) | 在当前位置插入签名行。 |
| [InsertSignatureLine](../../aspose.words/documentbuilder/insertsignatureline/#insertsignatureline_1)(SignatureLineOptions, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, WrapType) | 在指定位置插入签名行。 |
| [InsertStyleSeparator](../../aspose.words/documentbuilder/insertstyleseparator/)() | 将样式分隔符插入文档中。 |
| [InsertTableOfContents](../../aspose.words/documentbuilder/inserttableofcontents/)(string) | 将 TOC（目录）字段插入到文档中。 |
| [InsertTextInput](../../aspose.words/documentbuilder/inserttextinput/)(string, TextFormFieldType, string, string, int) | 在当前位置插入文本表单字段。 |
| [MoveTo](../../aspose.words/documentbuilder/moveto/)(Node) | 将光标移动到内联节点或段落末尾。 |
| [MoveToBookmark](../../aspose.words/documentbuilder/movetobookmark/#movetobookmark)(string) | 将光标移动到书签。 |
| [MoveToBookmark](../../aspose.words/documentbuilder/movetobookmark/#movetobookmark_1)(string, bool, bool) | 以更高精度将光标移动到书签。 |
| [MoveToCell](../../aspose.words/documentbuilder/movetocell/)(int, int, int, int) | 将光标移动到当前部分中的表格单元格。 |
| [MoveToDocumentEnd](../../aspose.words/documentbuilder/movetodocumentend/)() | 将光标移动到文档末尾。 |
| [MoveToDocumentStart](../../aspose.words/documentbuilder/movetodocumentstart/)() | 将光标移动到文档的开头。 |
| [MoveToField](../../aspose.words/documentbuilder/movetofield/)(Field, bool) | 将光标移动到文档中的字段。 |
| [MoveToHeaderFooter](../../aspose.words/documentbuilder/movetoheaderfooter/)(HeaderFooterType) | 将光标移动到当前节中页眉或页脚的开头。 |
| [MoveToMergeField](../../aspose.words/documentbuilder/movetomergefield/#movetomergefield)(string) | 将光标移动到指定合并字段之外的位置并删除合并字段。 |
| [MoveToMergeField](../../aspose.words/documentbuilder/movetomergefield/#movetomergefield_1)(string, bool, bool) | 将合并字段移动到指定的合并字段。 |
| [MoveToParagraph](../../aspose.words/documentbuilder/movetoparagraph/)(int, int) | 将光标移动到当前节中的段落。 |
| [MoveToSection](../../aspose.words/documentbuilder/movetosection/)(int) | 将光标移动到指定节中正文的开头。 |
| [MoveToStructuredDocumentTag](../../aspose.words/documentbuilder/movetostructureddocumenttag/#movetostructureddocumenttag_1)(int, int) | 将光标移动到当前部分中的结构化文档标记。 |
| [MoveToStructuredDocumentTag](../../aspose.words/documentbuilder/movetostructureddocumenttag/#movetostructureddocumenttag)(StructuredDocumentTag, int) | 将光标移至结构化文档标签。 |
| [PopFont](../../aspose.words/documentbuilder/popfont/)() | 检索先前保存在堆栈上的字符格式。 |
| [PushFont](../../aspose.words/documentbuilder/pushfont/)() | 将当前字符格式保存到堆栈上。 |
| [StartBookmark](../../aspose.words/documentbuilder/startbookmark/)(string) | 将文档中的当前位置标记为书签开始。 |
| [StartColumnBookmark](../../aspose.words/documentbuilder/startcolumnbookmark/)(string) | 将文档中的当前位置标记为列书签开始。该位置必须位于表格单元格中。 |
| [StartEditableRange](../../aspose.words/documentbuilder/starteditablerange/)() | 将文档中的当前位置标记为可编辑范围开始。 |
| [StartTable](../../aspose.words/documentbuilder/starttable/)() | 在文档中启动一个表格。 |
| [Write](../../aspose.words/documentbuilder/write/)(string) | 将字符串插入到文档中的当前插入位置。 |
| [Writeln](../../aspose.words/documentbuilder/writeln/#writeln)() | 在文档中插入段落分隔符。 |
| [Writeln](../../aspose.words/documentbuilder/writeln/#writeln_1)(string) | 将字符串和分段符插入到文档中。 |

### 评论

`DocumentBuilder`使得构建的过程[`Document`](../document/)更容易. [`Document`](../document/)是由节点树组成的复合对象，虽然可以将 content 节点直接插入树中，但需要很好地理解树结构。 `DocumentBuilder`是复杂结构的“外观”[`Document`](../document/)并允许 快速轻松地插入内容和格式。

创建一个`DocumentBuilder`并将其与[`Document`](../document/)。

这`DocumentBuilder`有一个内部光标，当您调用时，文本将被插入 [`Write`](./write/),[`Writeln`](./writeln/),[`InsertBreak`](./insertbreak/) 和其他方法。您可以导航`DocumentBuilder`使用各种 MoveToXXX 方法将光标移动到文档中的不同位置 。

使用[`Font`](./font/)属性来指定字符格式，该格式将应用于 从文档中当前位置开始插入的所有文本。

使用[`ParagraphFormat`](./paragraphformat/)属性来指定 current 和所有将插入的段落的段落格式。

使用[`PageSetup`](./pagesetup/)属性来指定 current 节和所有将插入的节的页面和节属性。

使用[`CellFormat`](./cellformat/)和[`RowFormat`](./rowformat/)属性来指定表单元格和行的 格式属性。用户[`InsertCell`](./insertcell/)和 [`EndRow`](./endrow/)建表的方法。

注意[`Font`](./font/),[`ParagraphFormat`](./paragraphformat/)和[`PageSetup`](./pagesetup/)只要 您导航到文档中的其他位置，属性就会更新，以反映新位置可用的格式属性。

### 例子

演示如何使用文档生成器创建表格。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 启动表格，然后用两个单元格填充第一行。
builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1.");
builder.InsertCell();
builder.Write("Row 1, Cell 2.");

// 调用构建器的“EndRow”方法来开始新行。
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, Cell 1.");
builder.InsertCell();
builder.Write("Row 2, Cell 2.");
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.CreateTable.docx");
```

演示如何使用 DocumentBuilder 在文档中创建页眉和页脚。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 指定我们希望首页、偶数页和奇数页使用不同的页眉和页脚。
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// 创建标题，然后向文档添加三个页面以显示每种标题类型。
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Write("Header for the first page");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Write("Header for even pages");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Header for all other pages");

builder.MoveToSection(0);
builder.Writeln("Page1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page3");

doc.Save(ArtifactsDir + "DocumentBuilder.HeadersAndFooters.docx");
```

演示如何构建具有自定义边框的表格。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

// 为文档生成器设置表格格式选项
// 将它们应用到我们添加的每一行和单元格。
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;

builder.CellFormat.ClearFormatting();
builder.CellFormat.Width = 150;
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.CellFormat.Shading.BackgroundPatternColor = Color.GreenYellow;
builder.CellFormat.WrapText = false;
builder.CellFormat.FitText = true;

builder.RowFormat.ClearFormatting();
builder.RowFormat.HeightRule = HeightRule.Exactly;
builder.RowFormat.Height = 50;
builder.RowFormat.Borders.LineStyle = LineStyle.Engrave3D;
builder.RowFormat.Borders.Color = Color.Orange;

builder.InsertCell();
builder.Write("Row 1, Col 1");

builder.InsertCell();
builder.Write("Row 1, Col 2");
builder.EndRow();

// 更改格式会将其应用到当前单元格，
// 以及我们随后使用构建器创建的任何新单元格。
// 这不会影响我们之前添加的单元格。
builder.CellFormat.Shading.ClearFormatting();

builder.InsertCell();
builder.Write("Row 2, Col 1");

builder.InsertCell();
builder.Write("Row 2, Col 2");

builder.EndRow();

// 增加行高以适合垂直文本。
builder.InsertCell();
builder.RowFormat.Height = 150;
builder.CellFormat.Orientation = TextOrientation.Upward;
builder.Write("Row 3, Col 1");

builder.InsertCell();
builder.CellFormat.Orientation = TextOrientation.Downward;
builder.Write("Row 3, Col 2");

builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTable.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)


