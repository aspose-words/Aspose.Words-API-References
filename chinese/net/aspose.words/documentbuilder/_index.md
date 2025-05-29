---
title: DocumentBuilder Class
linktitle: DocumentBuilder
articleTitle: DocumentBuilder
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.DocumentBuilder 类——轻松在文档中插入文本、图像和格式化元素的解决方案。
type: docs
weight: 660
url: /zh/net/aspose.words/documentbuilder/
---
## DocumentBuilder class

提供插入文本、图像和其他内容、指定字体、段落和章节格式的方法。

要了解更多信息，请访问[文档生成器概述](https://docs.aspose.com/words/net/document-builder-overview/)文档文章。

```csharp
public class DocumentBuilder
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [DocumentBuilder](documentbuilder/#constructor)() | 初始化此类的新实例。 |
| [DocumentBuilder](documentbuilder/#constructor_1)(*[Document](../document/)*) | 初始化此类的新实例。 |
| [DocumentBuilder](documentbuilder/#constructor_3)(*[DocumentBuilderOptions](../documentbuilderoptions/)*) | 初始化此类的新实例。 |
| [DocumentBuilder](documentbuilder/#constructor_2)(*[Document](../document/), [DocumentBuilderOptions](../documentbuilderoptions/)*) | 初始化此类的新实例。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Bold](../../aspose.words/documentbuilder/bold/) { get; set; } | 如果字体格式为粗体，则为真。 |
| [CellFormat](../../aspose.words/documentbuilder/cellformat/) { get; } | 返回表示当前表格单元格格式属性的对象。 |
| [CurrentNode](../../aspose.words/documentbuilder/currentnode/) { get; } | 获取此 DocumentBuilder 中当前选定的节点。 |
| [CurrentParagraph](../../aspose.words/documentbuilder/currentparagraph/) { get; } | 获取当前选中的段落`DocumentBuilder`. |
| [CurrentSection](../../aspose.words/documentbuilder/currentsection/) { get; } | 获取当前选中的部分`DocumentBuilder`. |
| [CurrentStory](../../aspose.words/documentbuilder/currentstory/) { get; } | 获取当前选中的故事`DocumentBuilder`. |
| [CurrentStructuredDocumentTag](../../aspose.words/documentbuilder/currentstructureddocumenttag/) { get; } | 获取当前选中的结构化文档标签`DocumentBuilder`. |
| [Document](../../aspose.words/documentbuilder/document/) { get; set; } | 获取或设置[`Document`](./document/)该对象所附加到的对象。 |
| [Font](../../aspose.words/documentbuilder/font/) { get; } | 返回表示当前字体格式属性的对象。 |
| [IsAtEndOfParagraph](../../aspose.words/documentbuilder/isatendofparagraph/) { get; } | 返回`真的`如果光标位于当前段落的末尾。 |
| [IsAtEndOfStructuredDocumentTag](../../aspose.words/documentbuilder/isatendofstructureddocumenttag/) { get; } | 返回**真的**如果光标位于结构化文档标签的末尾。 |
| [IsAtStartOfParagraph](../../aspose.words/documentbuilder/isatstartofparagraph/) { get; } | 返回`真的`如果光标位于当前段落的开头（光标前没有文本）。 |
| [Italic](../../aspose.words/documentbuilder/italic/) { get; set; } | 如果字体格式为斜体，则为真。 |
| [ListFormat](../../aspose.words/documentbuilder/listformat/) { get; } | 返回表示当前列表格式属性的对象。 |
| [PageSetup](../../aspose.words/documentbuilder/pagesetup/) { get; } | 返回代表当前页面设置和部分属性的对象。 |
| [ParagraphFormat](../../aspose.words/documentbuilder/paragraphformat/) { get; } | 返回表示当前段落格式属性的对象。 |
| [RowFormat](../../aspose.words/documentbuilder/rowformat/) { get; } | 返回表示当前表行格式属性的对象。 |
| [Underline](../../aspose.words/documentbuilder/underline/) { get; set; } | 获取/设置当前字体的下划线类型。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [DeleteRow](../../aspose.words/documentbuilder/deleterow/)(*int, int*) | 从表中删除一行。 |
| [EndBookmark](../../aspose.words/documentbuilder/endbookmark/)(*string*) | 将文档中的当前位置标记为书签结束。 |
| [EndColumnBookmark](../../aspose.words/documentbuilder/endcolumnbookmark/)(*string*) | 将文档中的当前位置标记为列书签的结束位置。该位置必须位于表格单元格中。 |
| [EndEditableRange](../../aspose.words/documentbuilder/endeditablerange/#endeditablerange)() | 将文档中的当前位置标记为可编辑范围的结束。 |
| [EndEditableRange](../../aspose.words/documentbuilder/endeditablerange/#endeditablerange_1)(*[EditableRangeStart](../editablerangestart/)*) | 将文档中的当前位置标记为可编辑范围的结束。 |
| [EndRow](../../aspose.words/documentbuilder/endrow/)() | 结束文档中的表格行。 |
| [EndTable](../../aspose.words/documentbuilder/endtable/)() | 结束文档中的表格。 |
| [InsertBreak](../../aspose.words/documentbuilder/insertbreak/)(*[BreakType](../breaktype/)*) | 在文档中插入指定类型的分隔符。 |
| [InsertCell](../../aspose.words/documentbuilder/insertcell/)() | 将表格单元格插入文档。 |
| [InsertChart](../../aspose.words/documentbuilder/insertchart/#insertchart_2)(*[ChartType](../../aspose.words.drawing.charts/charttype/), double, double*) | 将图表对象插入文档并将其缩放到指定大小。 |
| [InsertChart](../../aspose.words/documentbuilder/insertchart/#insertchart_3)(*[ChartType](../../aspose.words.drawing.charts/charttype/), double, double, [ChartStyle](../../aspose.words.drawing.charts/chartstyle/)*) | 将图表对象插入文档并将其缩放到指定大小。 |
| [InsertChart](../../aspose.words/documentbuilder/insertchart/#insertchart)(*[ChartType](../../aspose.words.drawing.charts/charttype/), [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | 将图表对象插入文档并将其缩放到指定大小。 |
| [InsertChart](../../aspose.words/documentbuilder/insertchart/#insertchart_1)(*[ChartType](../../aspose.words.drawing.charts/charttype/), [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/), [ChartStyle](../../aspose.words.drawing.charts/chartstyle/)*) | 将图表对象插入文档并将其缩放到指定大小。 |
| [InsertCheckBox](../../aspose.words/documentbuilder/insertcheckbox/#insertcheckbox_1)(*string, bool, int*) | 在当前位置插入复选框表单字段。 |
| [InsertCheckBox](../../aspose.words/documentbuilder/insertcheckbox/#insertcheckbox)(*string, bool, bool, int*) | 在当前位置插入复选框表单字段。 |
| [InsertComboBox](../../aspose.words/documentbuilder/insertcombobox/)(*string, string[], int*) | 在当前位置插入组合框表单字段。 |
| [InsertDocument](../../aspose.words/documentbuilder/insertdocument/#insertdocument)(*[Document](../document/), [ImportFormatMode](../importformatmode/)*) | 在光标位置插入文档。 |
| [InsertDocument](../../aspose.words/documentbuilder/insertdocument/#insertdocument_1)(*[Document](../document/), [ImportFormatMode](../importformatmode/), [ImportFormatOptions](../importformatoptions/)*) | 在光标位置插入文档。 |
| [InsertDocumentInline](../../aspose.words/documentbuilder/insertdocumentinline/)(*[Document](../document/), [ImportFormatMode](../importformatmode/), [ImportFormatOptions](../importformatoptions/)*) | 在光标位置插入内联文档。 |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield_1)(*string*) | 将 Word 字段插入文档并更新字段结果。 |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield)(*[FieldType](../../aspose.words.fields/fieldtype/), bool*) | 将 Word 字段插入文档并选择性地更新字段结果。 |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield_2)(*string, string*) | 将 Word 字段插入文档而不更新字段结果。 |
| [InsertFootnote](../../aspose.words/documentbuilder/insertfootnote/#insertfootnote)(*[FootnoteType](../../aspose.words.notes/footnotetype/), string*) | 在文档中插入脚注或尾注。 |
| [InsertFootnote](../../aspose.words/documentbuilder/insertfootnote/#insertfootnote_1)(*[FootnoteType](../../aspose.words.notes/footnotetype/), string, string*) | 在文档中插入脚注或尾注。 |
| [InsertForms2OleControl](../../aspose.words/documentbuilder/insertforms2olecontrol/)(*[Forms2OleControl](../../aspose.words.drawing.ole/forms2olecontrol/)*) | 插入[`Forms2OleControl`](../../aspose.words.drawing.ole/forms2olecontrol/)对象进入当前位置。 |
| [InsertGroupShape](../../aspose.words/documentbuilder/insertgroupshape/#insertgroupshape)(*params ShapeBase[]*) | 将作为参数传递的形状分组到插入当前位置的新 GroupShape 节点中。 |
| [InsertGroupShape](../../aspose.words/documentbuilder/insertgroupshape/#insertgroupshape_1)(*double, double, double, double, params ShapeBase[]*) | 将作为参数传递的形状分组到指定大小的新 GroupShape 节点中，然后插入到指定位置。 |
| [InsertHorizontalRule](../../aspose.words/documentbuilder/inserthorizontalrule/)() | 在文档中插入水平规则形状。 |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml)(*string*) | 将 HTML 字符串插入文档。 |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml_2)(*string, bool*) | 将 HTML 字符串插入文档。 |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml_1)(*string, [HtmlInsertOptions](../htmlinsertoptions/)*) | 在文档中插入 HTML 字符串。允许指定其他选项。 |
| [InsertHyperlink](../../aspose.words/documentbuilder/inserthyperlink/)(*string, string, bool*) | 在文档中插入超链接。 |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage)(*byte[]*) | 将字节数组中的图像插入文档。图像以内联方式插入，且比例为 100%。 |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_3)(*Image*) | 插入来自 .NET 的图像Image 对象插入文档。图像以 100% 比例内联插入。 |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_6)(*Stream*) | 将流中的图像插入文档。图像以内联方式插入，且比例为 100%。 |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_9)(*string*) | 将文件或 URL 中的图片插入文档。图片以内联方式插入，且比例为 100%。 |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_2)(*byte[], double, double*) | 将字节数组中的内联图像插入文档并将其缩放到指定大小。 |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_5)(*Image, double, double*) | 从 .NET 插入内联图像Image 对象放入文档并将其缩放到指定大小。 |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_8)(*Stream, double, double*) | 将流中的内嵌图像插入文档并将其缩放到指定大小。 |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_11)(*string, double, double*) | 将文件或 URL 中的内嵌图像插入文档并将其缩放到指定大小。 |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_1)(*byte[], [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | 在指定位置和大小插入字节数组中的图像。 |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_4)(*Image, [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | 插入来自 .NET 的图像Image位于指定位置和大小的 对象。 |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_7)(*Stream, [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | 将流中的图像插入到指定位置和大小。 |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_10)(*string, [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | 从文件或 URL 中插入指定位置和大小的图像。 |
| [InsertNode](../../aspose.words/documentbuilder/insertnode/)(*[Node](../node/)*) | 在光标前插入一个节点。 |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject)(*Stream, string, bool, Stream*) | 将嵌入的 OLE 对象从流插入到文档中。 |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject_1)(*string, bool, bool, Stream*) | 将文件中嵌入或链接的 OLE 对象插入文档。使用文件扩展名检测 OLE 对象类型。 |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject_2)(*string, string, bool, bool, Stream*) | 将文件中嵌入或链接的 OLE 对象插入文档。使用给定的 progID 参数检测 OLE 对象类型。 |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon)(*Stream, string, string, string*) | 将嵌入的 OLE 对象作为图标从流插入文档。 允许指定图标文件和标题。使用给定的 progID 参数检测 OLE 对象类型。 |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon_1)(*string, bool, string, string*) | 将嵌入或链接的 OLE 对象作为图标插入文档。 允许指定图标文件和标题。使用文件扩展名检测 OLE 对象类型。 |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon_2)(*string, string, bool, string, string*) | 将嵌入或链接的 OLE 对象作为图标插入文档。 允许指定图标文件和标题。使用给定的 progID 参数检测 OLE 对象类型。 |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_1)(*string, double, double*) | 将在线视频对象插入文档并将其缩放到指定大小。 |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_3)(*string, string, byte[], double, double*) | 将在线视频对象插入文档并将其缩放到指定大小。 |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo)(*string, [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | 将在线视频对象插入文档并将其缩放到指定大小。 |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_2)(*string, string, byte[], [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | 将在线视频对象插入文档并将其缩放到指定大小。 |
| [InsertParagraph](../../aspose.words/documentbuilder/insertparagraph/)() | 在文档中插入段落分隔符。 |
| [InsertShape](../../aspose.words/documentbuilder/insertshape/#insertshape_1)(*[ShapeType](../../aspose.words.drawing/shapetype/), double, double*) | 插入具有指定类型和大小的内联形状。 |
| [InsertShape](../../aspose.words/documentbuilder/insertshape/#insertshape)(*[ShapeType](../../aspose.words.drawing/shapetype/), [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | 插入具有指定位置、大小和文本换行类型的自由浮动形状。 |
| [InsertSignatureLine](../../aspose.words/documentbuilder/insertsignatureline/#insertsignatureline)(*[SignatureLineOptions](../signaturelineoptions/)*) | 在当前位置插入签名行。 |
| [InsertSignatureLine](../../aspose.words/documentbuilder/insertsignatureline/#insertsignatureline_1)(*[SignatureLineOptions](../signaturelineoptions/), [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, [WrapType](../../aspose.words.drawing/wraptype/)*) | 在指定位置插入签名行。 |
| [InsertStructuredDocumentTag](../../aspose.words/documentbuilder/insertstructureddocumenttag/)(*[SdtType](../../aspose.words.markup/sdttype/)*) | 插入[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/)进入文档。 |
| [InsertStyleSeparator](../../aspose.words/documentbuilder/insertstyleseparator/)() | 将样式分隔符插入文档。 |
| [InsertTableOfContents](../../aspose.words/documentbuilder/inserttableofcontents/)(*string*) | 将 TOC（目录）字段插入文档。 |
| [InsertTextInput](../../aspose.words/documentbuilder/inserttextinput/)(*string, [TextFormFieldType](../../aspose.words.fields/textformfieldtype/), string, string, int*) | 在当前位置插入文本表单字段。 |
| [MoveTo](../../aspose.words/documentbuilder/moveto/)(*[Node](../node/)*) | 将光标移动到内联节点或段落末尾。 |
| [MoveToBookmark](../../aspose.words/documentbuilder/movetobookmark/#movetobookmark)(*string*) | 将光标移动到书签。 |
| [MoveToBookmark](../../aspose.words/documentbuilder/movetobookmark/#movetobookmark_1)(*string, bool, bool*) | 将光标更精确地移动到书签。 |
| [MoveToCell](../../aspose.words/documentbuilder/movetocell/)(*int, int, int, int*) | 将光标移动到当前部分的表格单元格。 |
| [MoveToDocumentEnd](../../aspose.words/documentbuilder/movetodocumentend/)() | 将光标移动到文档末尾。 |
| [MoveToDocumentStart](../../aspose.words/documentbuilder/movetodocumentstart/)() | 将光标移动到文档的开头。 |
| [MoveToField](../../aspose.words/documentbuilder/movetofield/)(*[Field](../../aspose.words.fields/field/), bool*) | 将光标移动到文档中的某个字段。 |
| [MoveToHeaderFooter](../../aspose.words/documentbuilder/movetoheaderfooter/)(*[HeaderFooterType](../headerfootertype/)*) | 将光标移动到当前节的页眉或页脚的开头。 |
| [MoveToMergeField](../../aspose.words/documentbuilder/movetomergefield/#movetomergefield)(*string*) | 将光标移动到指定合并字段正前方的位置并删除合并字段。 |
| [MoveToMergeField](../../aspose.words/documentbuilder/movetomergefield/#movetomergefield_1)(*string, bool, bool*) | 将合并字段移动到指定的合并字段。 |
| [MoveToParagraph](../../aspose.words/documentbuilder/movetoparagraph/)(*int, int*) | 将光标移动到当前部分中的某个段落。 |
| [MoveToSection](../../aspose.words/documentbuilder/movetosection/)(*int*) | 将光标移动到指定部分正文的开头。 |
| [MoveToStructuredDocumentTag](../../aspose.words/documentbuilder/movetostructureddocumenttag/#movetostructureddocumenttag_1)(*int, int*) | 将光标移动到当前部分的结构化文档标签。 |
| [MoveToStructuredDocumentTag](../../aspose.words/documentbuilder/movetostructureddocumenttag/#movetostructureddocumenttag)(*[StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/), int*) | 将光标移动到结构化文档标签。 |
| [PopFont](../../aspose.words/documentbuilder/popfont/)() | 检索先前保存在堆栈上的字符格式。 |
| [PushFont](../../aspose.words/documentbuilder/pushfont/)() | 将当前字符格式保存到堆栈上。 |
| [StartBookmark](../../aspose.words/documentbuilder/startbookmark/)(*string*) | 将文档中的当前位置标记为书签的起始位置。 |
| [StartColumnBookmark](../../aspose.words/documentbuilder/startcolumnbookmark/)(*string*) | 将文档中的当前位置标记为列书签的起始位置。该位置必须位于表格单元格中。 |
| [StartEditableRange](../../aspose.words/documentbuilder/starteditablerange/)() | 将文档中的当前位置标记为可编辑范围的开始。 |
| [StartTable](../../aspose.words/documentbuilder/starttable/)() | 在文档中开始一个表格。 |
| [Write](../../aspose.words/documentbuilder/write/)(*string*) | 在文档的当前插入位置插入一个字符串。 |
| [Writeln](../../aspose.words/documentbuilder/writeln/#writeln)() | 在文档中插入段落分隔符。 |
| [Writeln](../../aspose.words/documentbuilder/writeln/#writeln_1)(*string*) | 在文档中插入字符串和段落分隔符。 |

## 评论

`DocumentBuilder`使构建过程[`Document`](../document/)更容易。 [`Document`](../document/)是由节点树组成的复合对象，虽然可以将 content 节点直接插入树中，但这需要很好地理解树结构。 `DocumentBuilder`是复杂结构的“外观”[`Document`](../document/)并允许 快速轻松地插入内容和格式。

创建一个`DocumentBuilder`并将其与[`Document`](../document/)。

这`DocumentBuilder`有一个内部光标，当您调用时，文本将插入其中 [`Write`](./write/)，[`Writeln`](./writeln/)，[`InsertBreak`](./insertbreak/) 和其他方法。您可以导航`DocumentBuilder`使用各种 MoveToXXX 方法将光标移动到文档中的不同 location 。

使用[`Font`](./font/)属性来指定将应用于 从文档中的当前位置开始插入的所有文本的字符格式。

使用[`ParagraphFormat`](./paragraphformat/)属性来指定 current 和所有将插入的段落的段落格式。

使用[`PageSetup`](./pagesetup/)属性来指定 current 部分和将插入的所有部分的页面和部分属性。

使用[`CellFormat`](./cellformat/)和[`RowFormat`](./rowformat/)属性来指定表格单元格和行的格式属性。用户[`InsertCell`](./insertcell/)and [`EndRow`](./endrow/)建立表的方法。

注意[`Font`](./font/)，[`ParagraphFormat`](./paragraphformat/)和[`PageSetup`](./pagesetup/)每当您导航到文档中的其他位置时，属性都会更新，以反映新位置可用的格式属性。

## 例子

展示如何使用文档生成器创建表格。

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

展示如何使用 DocumentBuilder 在文档中创建页眉和页脚。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 指定我们希望第一页、偶数页和奇数页使用不同的页眉和页脚。
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// 创建页眉，然后向文档添加三页以显示每种页眉类型。
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

展示如何构建具有自定义边框的表格。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

// 为文档生成器设置表格格式选项
// 将它们应用于我们添加的每一行和单元格。
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

// 更改格式将应用于当前单元格，
// 以及我们随后使用构建器创建的任何新单元格。
// 这不会影响我们之前添加的单元格。
builder.CellFormat.Shading.ClearFormatting();

builder.InsertCell();
builder.Write("Row 2, Col 1");

builder.InsertCell();
builder.Write("Row 2, Col 2");

builder.EndRow();

// 增加行高以适应垂直文本。
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
