---
title: "Aspose::Words::DocumentBuilder 类"
linktitle: "DocumentBuilder"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBuilder 类。提供插入文本、图像和其他内容、指定字体、段落和章节格式的方法。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 22000
url: /zh/cpp/aspose.words/documentbuilder/
---
## DocumentBuilder class


提供插入文本、图像和其他内容、指定字体、段落和章节格式的方法。要了解更多信息，请访问 [Document Builder Overview](https://docs.aspose.com/words/cpp/document-builder-overview/) 文档文章。

```cpp
class DocumentBuilder : public Aspose::Words::IRunAttrSource,
                        public Aspose::Words::IParaAttrSource,
                        public Aspose::Words::IRowAttrSource,
                        public Aspose::Words::ICellAttrSource
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [DeleteRow](./deleterow/)(int32_t, int32_t) | 删除表中的一行。 |
| [DocumentBuilder](./documentbuilder/)() | 初始化此类的新实例。 |
| [DocumentBuilder](./documentbuilder/)(const System::SharedPtr\<Aspose::Words::DocumentBuilderOptions\>\&) | 初始化此类的新实例。 |
| [DocumentBuilder](./documentbuilder/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | 初始化此类的新实例。 |
| [DocumentBuilder](./documentbuilder/)(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::SharedPtr\<Aspose::Words::DocumentBuilderOptions\>\&) | 初始化此类的新实例。 |
| [EndBookmark](./endbookmark/)(const System::String\&) | 将文档中的当前位置标记为书签结束。 |
| [EndColumnBookmark](./endcolumnbookmark/)(const System::String\&) | 将文档中当前位置标记为列书签结束。该位置必须位于表格单元格中。 |
| [EndEditableRange](./endeditablerange/)() | 将文档中当前位置标记为可编辑范围结束。 |
| [EndEditableRange](./endeditablerange/)(const System::SharedPtr\<Aspose::Words::EditableRangeStart\>\&) | 将文档中当前位置标记为可编辑范围结束。 |
| [EndRow](./endrow/)() | 结束文档中的表格行。 |
| [EndTable](./endtable/)() | 结束文档中的表格。 |
| [get_Bold](./get_bold/)() | 如果字体设置为粗体，则为 True。 |
| [get_CellFormat](./get_cellformat/)() | 返回表示当前表格单元格格式属性的对象。 |
| [get_CurrentNode](./get_currentnode/)() | 获取当前在此 [DocumentBuilder](./) 中选中的节点。 |
| [get_CurrentParagraph](./get_currentparagraph/)() | 获取当前在此 [DocumentBuilder](./) 中选中的段落。 |
| [get_CurrentSection](./get_currentsection/)() | 获取当前在此 [DocumentBuilder](./) 中选中的节。 |
| [get_CurrentStory](./get_currentstory/)() | 获取当前在此 [DocumentBuilder](./) 中选中的故事。 |
| [get_CurrentStructuredDocumentTag](./get_currentstructureddocumenttag/)() | 获取当前在此 [DocumentBuilder](./) 中选中的结构化文档标签。 |
| [get_Document](./get_document/)() const | 获取或设置此对象所附加的 [Document](./get_document/) 对象。 |
| [get_Font](./get_font/)() | 返回表示当前字体格式属性的对象。 |
| [get_IsAtEndOfParagraph](./get_isatendofparagraph/)() | 如果光标位于当前段落的末尾，则返回 **true**。 |
| [get_IsAtEndOfStructuredDocumentTag](./get_isatendofstructureddocumenttag/)() | 如果光标位于结构化文档标签的末尾，则返回 **true**。 |
| [get_IsAtStartOfParagraph](./get_isatstartofparagraph/)() | 如果光标位于当前段落的开头（光标前没有文本），则返回 **true**。 |
| [get_Italic](./get_italic/)() | 如果字体设置为斜体，则为 True。 |
| [get_ListFormat](./get_listformat/)() | 返回表示当前列表格式属性的对象。 |
| [get_PageSetup](./get_pagesetup/)() | 返回表示当前页面设置和节属性的对象。 |
| [get_ParagraphFormat](./get_paragraphformat/)() | 返回表示当前段落格式属性的对象。 |
| [get_RowFormat](./get_rowformat/)() | 返回表示当前表格行格式属性的对象。 |
| [get_Underline](./get_underline/)() | 获取/设置当前字体的下划线类型。 |
| [GetType](./gettype/)() const override |  |
| [InsertBreak](./insertbreak/)(Aspose::Words::BreakType) | 在文档中插入指定类型的换页符。 |
| [InsertCell](./insertcell/)() | 在文档中插入表格单元格。 |
| [InsertChart](./insertchart/)(Aspose::Words::Drawing::Charts::ChartType, double, double) | 在文档中插入图表对象并将其缩放到指定大小。 |
| [InsertChart](./insertchart/)(Aspose::Words::Drawing::Charts::ChartType, double, double, Aspose::Words::Drawing::Charts::ChartStyle) | 在文档中插入图表对象并将其缩放到指定大小。 |
| [InsertChart](./insertchart/)(Aspose::Words::Drawing::Charts::ChartType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | 在文档中插入图表对象并将其缩放到指定大小。 |
| [InsertChart](./insertchart/)(Aspose::Words::Drawing::Charts::ChartType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType, Aspose::Words::Drawing::Charts::ChartStyle) | 在文档中插入图表对象并将其缩放到指定大小。 |
| [InsertCheckBox](./insertcheckbox/)(const System::String\&, bool, int32_t) | 在当前位置插入复选框表单字段。 |
| [InsertCheckBox](./insertcheckbox/)(const System::String\&, bool, bool, int32_t) | 在当前位置插入复选框表单字段。 |
| [InsertComboBox](./insertcombobox/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, int32_t) | 在当前位置插入下拉框表单字段。 |
| [InsertDocument](./insertdocument/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode) | 在光标位置插入文档。 |
| [InsertDocument](./insertdocument/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | 在光标位置插入文档。 |
| [InsertDocumentInline](./insertdocumentinline/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | 在光标位置内联插入文档。 |
| [InsertField](./insertfield/)(Aspose::Words::Fields::FieldType, bool) | 将 Word 字段插入文档，并可选择性更新字段结果。 |
| [InsertField](./insertfield/)(const System::String\&) | 将 Word 字段插入文档并更新字段结果。 |
| [InsertField](./insertfield/)(const System::String\&, const System::String\&) | 将 Word 字段插入文档但不更新字段结果。 |
| [InsertFootnote](./insertfootnote/)(Aspose::Words::Notes::FootnoteType, const System::String\&) | 在文档中插入脚注或尾注。 |
| [InsertFootnote](./insertfootnote/)(Aspose::Words::Notes::FootnoteType, const System::String\&, const System::String\&) | 在文档中插入脚注或尾注。 |
| [InsertForms2OleControl](./insertforms2olecontrol/)(const System::SharedPtr\<Aspose::Words::Drawing::Ole::Forms2OleControl\>\&) | 在当前位置插入 [Forms2OleControl](../) 对象。 |
| [InsertGroupShape](./insertgroupshape/)(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\>\&) | 将作为参数传入的形状分组为新的 GroupShape 节点，并插入到当前位置。 |
| [InsertGroupShape](./insertgroupshape/)(double, double, double, double, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\>\&) | 将作为参数传入的形状分组为指定大小的新 GroupShape 节点，并插入到指定位置。 |
| [InsertHorizontalRule](./inserthorizontalrule/)() | 在文档中插入水平线形状。 |
| [InsertHtml](./inserthtml/)(const System::String\&) | 将 HTML 字符串插入文档。 |
| [InsertHtml](./inserthtml/)(const System::String\&, bool) | 将 HTML 字符串插入文档。 |
| [InsertHtml](./inserthtml/)(const System::String\&, Aspose::Words::HtmlInsertOptions) | 将 HTML 字符串插入文档。允许指定其他选项。 |
| [InsertHyperlink](./inserthyperlink/)(const System::String\&, const System::String\&, bool) | 在文档中插入超链接。 |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::Drawing::Image\>\&) | 从 **Image** 对象插入图像到文档。图像以内联方式插入，比例为 100%。 |
| [InsertImage](./insertimage/)(const System::String\&) | 从文件或 URL 插入图像到文档。图像以内联方式插入，比例为 100%。 |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::IO::Stream\>\&) | 从流插入图像到文档。图像以内联方式插入，比例为 100%。 |
| [InsertImage](./insertimage/)(const System::ArrayPtr\<uint8_t\>\&) | 从字节数组插入图像到文档。图像以内联方式插入，比例为 100%。 |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::Drawing::Image\>\&, double, double) | 从 **Image** 对象插入内联图像到文档，并按指定尺寸缩放。 |
| [InsertImage](./insertimage/)(const System::String\&, double, double) | 从文件或 URL 插入内联图像到文档，并按指定尺寸缩放。 |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::IO::Stream\>\&, double, double) | 从流插入内联图像到文档，并按指定尺寸缩放。 |
| [InsertImage](./insertimage/)(const System::ArrayPtr\<uint8_t\>\&, double, double) | 从字节数组插入内联图像到文档，并按指定尺寸缩放。 |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::Drawing::Image\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | 从 **Image** 对象在指定位置和尺寸插入图像。 |
| [InsertImage](./insertimage/)(const System::String\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | 从文件或 URL 在指定位置和尺寸插入图像。 |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | 在指定的位置和大小插入来自流的图像。 |
| [InsertImage](./insertimage/)(const System::ArrayPtr\<uint8_t\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | 在指定的位置和大小插入来自字节数组的图像。 |
| [InsertImage](./insertimage/)(std::basic_istream\<CharType, Traits\>\&) |  |
| [InsertImage](./insertimage/)(std::basic_istream\<CharType, Traits\>\&, double, double) |  |
| [InsertImage](./insertimage/)(std::basic_istream\<CharType, Traits\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) |  |
| [InsertNode](./insertnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 在光标前插入节点。 |
| [InsertOleObject](./insertoleobject/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::String\&, bool, const System::SharedPtr\<System::IO::Stream\>\&) | 从流中插入嵌入的 OLE 对象到文档中。 |
| [InsertOleObject](./insertoleobject/)(const System::String\&, bool, bool, const System::SharedPtr\<System::IO::Stream\>\&) | 从文件中插入嵌入或链接的 OLE 对象到文档中。使用文件扩展名检测 OLE 对象类型。 |
| [InsertOleObject](./insertoleobject/)(const System::String\&, const System::String\&, bool, bool, const System::SharedPtr\<System::IO::Stream\>\&) | 从文件中插入嵌入或链接的 OLE 对象到文档中。使用给定的 progID 参数检测 OLE 对象类型。 |
| [InsertOleObject](./insertoleobject/)(std::basic_istream\<CharType, Traits\>\&, System::String, bool, std::basic_istream\<CharType, Traits\>\&) |  |
| [InsertOleObject](./insertoleobject/)(System::String, bool, bool, std::basic_istream\<CharType, Traits\>\&) |  |
| [InsertOleObject](./insertoleobject/)(System::String, System::String, bool, bool, std::basic_istream\<CharType, Traits\>\&) |  |
| [InsertOleObjectAsIcon](./insertoleobjectasicon/)(const System::String\&, bool, const System::String\&, const System::String\&) | 将嵌入或链接的 OLE 对象作为图标插入文档中。允许指定图标文件和标题。使用文件扩展名检测 OLE 对象类型。 |
| [InsertOleObjectAsIcon](./insertoleobjectasicon/)(const System::String\&, const System::String\&, bool, const System::String\&, const System::String\&) | 将嵌入或链接的 OLE 对象作为图标插入文档中。允许指定图标文件和标题。使用给定的 progID 参数检测 OLE 对象类型。 |
| [InsertOleObjectAsIcon](./insertoleobjectasicon/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::String\&, const System::String\&, const System::String\&) | 从流中将嵌入的 OLE 对象作为图标插入文档中。允许指定图标文件和标题。使用给定的 progID 参数检测 OLE 对象类型。 |
| [InsertOleObjectAsIcon](./insertoleobjectasicon/)(std::basic_istream\<CharType, Traits\>\&, System::String, System::String, System::String) |  |
| [InsertOnlineVideo](./insertonlinevideo/)(const System::String\&, double, double) | 将在线视频对象插入文档并按指定大小缩放。 |
| [InsertOnlineVideo](./insertonlinevideo/)(const System::String\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | 将在线视频对象插入文档并按指定大小缩放。 |
| [InsertOnlineVideo](./insertonlinevideo/)(const System::String\&, const System::String\&, const System::ArrayPtr\<uint8_t\>\&, double, double) | 将在线视频对象插入文档并按指定大小缩放。 |
| [InsertOnlineVideo](./insertonlinevideo/)(const System::String\&, const System::String\&, const System::ArrayPtr\<uint8_t\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | 将在线视频对象插入文档并按指定大小缩放。 |
| [InsertParagraph](./insertparagraph/)() | 在文档中插入段落换行符。 |
| [InsertShape](./insertshape/)(Aspose::Words::Drawing::ShapeType, double, double) | 插入具有指定类型和大小的内联形状。 |
| [InsertShape](./insertshape/)(Aspose::Words::Drawing::ShapeType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | 插入具有指定位置、大小和文本环绕类型的自由浮动形状。 |
| [InsertSignatureLine](./insertsignatureline/)(const System::SharedPtr\<Aspose::Words::SignatureLineOptions\>\&) | 在当前位置插入签名行。 |
| [InsertSignatureLine](./insertsignatureline/)(const System::SharedPtr\<Aspose::Words::SignatureLineOptions\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, Aspose::Words::Drawing::WrapType) | 在指定位置插入签名行。 |
| [InsertStructuredDocumentTag](./insertstructureddocumenttag/)(Aspose::Words::Markup::SdtType) | 在文档中插入一个 [StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/)。 |
| [InsertStyleSeparator](./insertstyleseparator/)() | 在文档中插入样式分隔符。 |
| [InsertTableOfContents](./inserttableofcontents/)(const System::String\&) | 在文档中插入 TOC（目录）字段。 |
| [InsertTextInput](./inserttextinput/)(const System::String\&, Aspose::Words::Fields::TextFormFieldType, const System::String\&, const System::String\&, int32_t) | 在当前位置插入文本表单字段。 |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [MoveTo](./moveto/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 将光标移动到内联节点或段落末尾。 |
| [MoveToBookmark](./movetobookmark/)(const System::String\&) | 将光标移动到书签。 |
| [MoveToBookmark](./movetobookmark/)(const System::String\&, bool, bool) | 将光标更精确地移动到书签。 |
| [MoveToCell](./movetocell/)(int32_t, int32_t, int32_t, int32_t) | 将光标移动到当前节中的表格单元格。 |
| [MoveToDocumentEnd](./movetodocumentend/)() | 将光标移动到文档末尾。 |
| [MoveToDocumentStart](./movetodocumentstart/)() | 将光标移动到文档开头。 |
| [MoveToField](./movetofield/)(const System::SharedPtr\<Aspose::Words::Fields::Field\>\&, bool) | 将光标移动到文档中的字段。 |
| [MoveToHeaderFooter](./movetoheaderfooter/)(Aspose::Words::HeaderFooterType) | 将光标移动到当前节的页眉或页脚的开头。 |
| [MoveToMergeField](./movetomergefield/)(const System::String\&) | 将光标移动到指定合并域之后的位置，并删除该合并域。 |
| [MoveToMergeField](./movetomergefield/)(const System::String\&, bool, bool) | 将合并域移动到指定的合并域。 |
| [MoveToParagraph](./movetoparagraph/)(int32_t, int32_t) | 将光标移动到当前节中的段落。 |
| [MoveToSection](./movetosection/)(int32_t) | 将光标移动到指定节正文的开头。 |
| [MoveToStructuredDocumentTag](./movetostructureddocumenttag/)(int32_t, int32_t) | 将光标移动到当前节中的结构化文档标签。 |
| [MoveToStructuredDocumentTag](./movetostructureddocumenttag/)(const System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTag\>\&, int32_t) | 将光标移动到结构化文档标签。 |
| [PopFont](./popfont/)() | 检索先前保存在堆栈上的字符格式。 |
| [PushFont](./pushfont/)() | 将当前字符格式保存到堆栈上。 |
| [set_Bold](./set_bold/)(bool) | 设置 [Aspose::Words::DocumentBuilder::get_Bold](./get_bold/)。 |
| [set_Document](./set_document/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | 设置 [Aspose::Words::DocumentBuilder::get_Document](./get_document/)。 |
| [set_Italic](./set_italic/)(bool) | 设置 [Aspose::Words::DocumentBuilder::get_Italic](./get_italic/)。 |
| [set_Underline](./set_underline/)(Aspose::Words::Underline) | 设置 [Aspose::Words::DocumentBuilder::get_Underline](./get_underline/)。 |
| [StartBookmark](./startbookmark/)(const System::String\&) | 将文档中当前位置标记为书签起始位置。 |
| [StartColumnBookmark](./startcolumnbookmark/)(const System::String\&) | 将文档中当前位置标记为列书签起始位置。该位置必须位于表格单元格中。 |
| [StartEditableRange](./starteditablerange/)() | 将文档中当前位置标记为可编辑范围的起始位置。 |
| [StartTable](./starttable/)() | 在文档中开始一个表格。 |
| static [Type](./type/)() |  |
| [Write](./write/)(const System::String\&) | 在当前插入位置向文档插入字符串。 |
| [Writeln](./writeln/)(const System::String\&) | 向文档插入字符串和段落换行。 |
| [Writeln](./writeln/)() | 在文档中插入段落换行符。 |
## 备注


[DocumentBuilder](./) makes the process of building a [Document](../document/) easier. [Document](../document/) is a composite object consisting of a tree of nodes and while inserting content nodes directly into the tree is possible, it requires good understanding of the tree structure. [DocumentBuilder](./) is a "facade" for the complex structure of [Document](../document/) and allows to insert content and formatting quickly and easily.

创建一个 [DocumentBuilder](./) 并将其关联到一个 [Document](../document/)。

[DocumentBuilder](./) 有一个内部光标，当您调用 [Write()](../)、[Writeln()](../)、[InsertBreak()](./insertbreak/) 等方法时，文本将插入到该光标位置。您可以使用各种 MoveToXXX 方法将 [DocumentBuilder](./) 光标导航到文档中的其他位置。

使用 [Font](./get_font/) 属性指定字符格式，该格式将应用于从文档中当前位置起插入的所有文本。

使用 [ParagraphFormat](./get_paragraphformat/) 属性指定段落格式，适用于当前段落以及所有将要插入的段落。

使用 [PageSetup](./get_pagesetup/) 属性指定页面和节的属性，适用于当前节以及所有将要插入的节。

使用 [CellFormat](./get_cellformat/) 和 [RowFormat](./get_rowformat/) 属性来指定表格单元格和行的格式属性。使用 [InsertCell](./insertcell/) 和 [EndRow](./endrow/) 方法来构建表格。

请注意，[Font](./get_font/)、[ParagraphFormat](./get_paragraphformat/) 和 [PageSetup](./get_pagesetup/) 属性会在您在文档中导航到不同位置时更新，以反映新位置可用的格式属性。

## 示例



展示如何使用自定义边框构建表格。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartTable();

// 为文档生成器设置表格格式选项
// 它们将应用于我们使用它添加的每一行和每个单元格。
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

builder->get_CellFormat()->ClearFormatting();
builder->get_CellFormat()->set_Width(150);
builder->get_CellFormat()->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_GreenYellow());
builder->get_CellFormat()->set_WrapText(false);
builder->get_CellFormat()->set_FitText(true);

builder->get_RowFormat()->ClearFormatting();
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Exactly);
builder->get_RowFormat()->set_Height(50);
builder->get_RowFormat()->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Engrave3D);
builder->get_RowFormat()->get_Borders()->set_Color(System::Drawing::Color::get_Orange());

builder->InsertCell();
builder->Write(u"Row 1, Col 1");

builder->InsertCell();
builder->Write(u"Row 1, Col 2");
builder->EndRow();

// 更改格式将应用于当前单元格，
// 以及随后使用生成器创建的任何新单元格。
// 这不会影响我们之前添加的单元格。
builder->get_CellFormat()->get_Shading()->ClearFormatting();

builder->InsertCell();
builder->Write(u"Row 2, Col 1");

builder->InsertCell();
builder->Write(u"Row 2, Col 2");

builder->EndRow();

// 增加行高以适应竖排文本。
builder->InsertCell();
builder->get_RowFormat()->set_Height(150);
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Upward);
builder->Write(u"Row 3, Col 1");

builder->InsertCell();
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Downward);
builder->Write(u"Row 3, Col 2");

builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTable.docx");
```


展示如何使用文档生成器创建表格。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 开始表格，然后用两个单元格填充第一行。
builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, Cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, Cell 2.");

// 调用生成器的 "EndRow" 方法以开始新行。
builder->EndRow();
builder->InsertCell();
builder->Write(u"Row 2, Cell 1.");
builder->InsertCell();
builder->Write(u"Row 2, Cell 2.");
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.CreateTable.docx");
```

## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
