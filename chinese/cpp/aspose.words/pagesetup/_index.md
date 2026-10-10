---
title: "Aspose::Words::PageSetup 类"
linktitle: "PageSetup"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::PageSetup 类。表示节的页面设置属性。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 46000
url: /zh/cpp/aspose.words/pagesetup/
---
## PageSetup class


表示节的页面设置属性。要了解更多，请访问 [Working with Sections](https://docs.aspose.com/words/cpp/working-with-sections/) 文档文章。

```cpp
class PageSetup : public Aspose::Words::IBorderAttrSource
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | 将页面设置重置为默认的纸张尺寸、页边距和方向。 |
| [get_Bidi](./get_bidi/)() | 指定此节包含双向（复杂脚本）文本。 |
| [get_BorderAlwaysInFront](./get_borderalwaysinfront/)() | 指定页面边框相对于交叉文本和对象的位置。 |
| [get_BorderAppliesTo](./get_borderappliesto/)() | 指定页面边框打印的页面。 |
| [get_BorderDistanceFrom](./get_borderdistancefrom/)() | 获取或设置一个值，指示指定的页面边框是从页面边缘还是从其包围的文本测量。 |
| [get_Borders](./get_borders/)() | 获取页面边框的集合。 |
| [get_BorderSurroundsFooter](./get_bordersurroundsfooter/)() | 指定页面边框是否包括或排除页脚。 |
| [get_BorderSurroundsHeader](./get_bordersurroundsheader/)() | 指定页面边框是否包括或排除页眉。 |
| [get_BottomMargin](./get_bottommargin/)() | 返回或设置页面底部边缘与正文底部边界之间的距离（以点为单位）。 |
| [get_ChapterPageSeparator](./get_chapterpageseparator/)() | 获取或设置出现在章节号和页码之间的分隔符字符。 |
| [get_CharactersPerLine](./get_charactersperline/)() | 获取或设置文档网格中每行的字符数。 |
| [get_DifferentFirstPageHeaderFooter](./get_differentfirstpageheaderfooter/)() | 如果首页使用不同的页眉或页脚，则为 true。 |
| [get_EndnoteOptions](./get_endnoteoptions/)() | 提供控制本节尾注编号和位置的选项。 |
| [get_FirstPageTray](./get_firstpagetray/)() | 获取用于节的首页的纸盘（纸盒）。该值取决于实现（打印机）。 |
| [get_FooterDistance](./get_footerdistance/)() | 返回或设置页脚与页面底部之间的距离（以点为单位）。 |
| [get_FootnoteOptions](./get_footnoteoptions/)() | 提供控制本节脚注编号和位置的选项。 |
| [get_Gutter](./get_gutter/)() | 获取或设置为文档装订在页边距中添加的额外空间量。 |
| [get_HeaderDistance](./get_headerdistance/)() | 返回或设置页眉与页面顶部之间的距离（以点为单位）。 |
| [get_HeadingLevelForChapter](./get_headinglevelforchapter/)() | 获取或设置应用于文档章节标题的标题级别样式。 |
| [get_LayoutMode](./get_layoutmode/)() | 获取或设置本节的布局模式。 |
| [get_LeftMargin](./get_leftmargin/)() | 返回或设置页面左边缘与正文左边界之间的距离（以点为单位）。 |
| [get_LineNumberCountBy](./get_linenumbercountby/)() | 返回或设置行号的数值增量。 |
| [get_LineNumberDistanceFromText](./get_linenumberdistancefromtext/)() | 获取或设置行号右边缘与文档左边缘之间的距离。 |
| [get_LineNumberRestartMode](./get_linenumberrestartmode/)() | 获取或设置行号的计数方式，即它是在新页面或新节的开头重新开始，还是连续计数。 |
| [get_LinesPerPage](./get_linesperpage/)() | 获取或设置文档网格中每页的行数。 |
| [get_LineStartingNumber](./get_linestartingnumber/)() | 获取或设置起始行号。 |
| [get_Margins](./get_margins/)() | 返回或设置页面的预设 [Margins](../margins/)。 |
| [get_MultiplePages](./get_multiplepages/)() const | 对于多页文档，获取或设置文档的打印或渲染方式，以便可以装订成小册子。 |
| [get_OddAndEvenPagesHeaderFooter](./get_oddandevenpagesheaderfooter/)() const | 如果文档对奇数页和偶数页使用不同的页眉和页脚，则为 true。 |
| [get_Orientation](./get_orientation/)() | 返回或设置页面的方向。 |
| [get_OtherPagesTray](./get_otherpagestray/)() | 获取用于章节除第一页之外所有页面的纸盘（纸盒）。该值取决于实现（打印机）。 |
| [get_PageHeight](./get_pageheight/)() | 返回或设置页面的高度（单位为点）。 |
| [get_PageNumberStyle](./get_pagenumberstyle/)() | 获取或设置页码格式。 |
| [get_PageStartingNumber](./get_pagestartingnumber/)() | 获取或设置章节的起始页码。 |
| [get_PageWidth](./get_pagewidth/)() | 返回或设置页面的宽度（单位为点）。 |
| [get_PaperSize](./get_papersize/)() | 返回或设置纸张尺寸。 |
| [get_RestartPageNumbering](./get_restartpagenumbering/)() | 如果页码在章节开头重新开始，则为 true。 |
| [get_RightMargin](./get_rightmargin/)() | 返回或设置页面右边缘与正文右边界之间的距离（单位为点）。 |
| [get_RtlGutter](./get_rtlgutter/)() | 获取或设置 Microsoft Word 是否根据从右到左语言或从左到右语言为章节使用装订线。 |
| [get_SectionStart](./get_sectionstart/)() | 返回或设置指定对象的分节符类型。 |
| [get_SheetsPerBooklet](./get_sheetsperbooklet/)() const | 返回或设置每本小册子包含的页数。 |
| [get_SuppressEndnotes](./get_suppressendnotes/)() | 如果尾注打印在下一个未抑制尾注的章节末尾，则为 true。被抑制的尾注会在该章节的尾注之前打印。 |
| [get_TextColumns](./get_textcolumns/)() | 返回表示文本列集合的集合。 |
| [get_TextOrientation](./get_textorientation/)() | 允许为整页指定 [TextOrientation](./get_textorientation/)。默认值是 [Horizontal](../textorientation/)。 |
| [get_TopMargin](./get_topmargin/)() | 返回或设置页面顶部边缘与正文顶部边界之间的距离（单位为点）。 |
| [get_VerticalAlignment](./get_verticalalignment/)() | 返回或设置文档或章节中每页文本的垂直对齐方式。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Bidi](./set_bidi/)(bool) | 用于设置 [Aspose::Words::PageSetup::get_Bidi](./get_bidi/). |
| [set_BorderAlwaysInFront](./set_borderalwaysinfront/)(bool) | 用于设置 [Aspose::Words::PageSetup::get_BorderAlwaysInFront](./get_borderalwaysinfront/). |
| [set_BorderAppliesTo](./set_borderappliesto/)(Aspose::Words::PageBorderAppliesTo) | 用于设置 [Aspose::Words::PageSetup::get_BorderAppliesTo](./get_borderappliesto/). |
| [set_BorderDistanceFrom](./set_borderdistancefrom/)(Aspose::Words::PageBorderDistanceFrom) | 用于设置 [Aspose::Words::PageSetup::get_BorderDistanceFrom](./get_borderdistancefrom/). |
| [set_BorderSurroundsFooter](./set_bordersurroundsfooter/)(bool) | 用于设置 [Aspose::Words::PageSetup::get_BorderSurroundsFooter](./get_bordersurroundsfooter/). |
| [set_BorderSurroundsHeader](./set_bordersurroundsheader/)(bool) | 用于设置 [Aspose::Words::PageSetup::get_BorderSurroundsHeader](./get_bordersurroundsheader/). |
| [set_BottomMargin](./set_bottommargin/)(double) | 用于设置 [Aspose::Words::PageSetup::get_BottomMargin](./get_bottommargin/). |
| [set_ChapterPageSeparator](./set_chapterpageseparator/)(Aspose::Words::ChapterPageSeparator) | 用于设置 [Aspose::Words::PageSetup::get_ChapterPageSeparator](./get_chapterpageseparator/). |
| [set_CharactersPerLine](./set_charactersperline/)(int32_t) | 用于设置 [Aspose::Words::PageSetup::get_CharactersPerLine](./get_charactersperline/). |
| [set_DifferentFirstPageHeaderFooter](./set_differentfirstpageheaderfooter/)(bool) | 用于设置 [Aspose::Words::PageSetup::get_DifferentFirstPageHeaderFooter](./get_differentfirstpageheaderfooter/). |
| [set_FirstPageTray](./set_firstpagetray/)(int32_t) | 设置章节第一页使用的纸盘（托盘）。该值取决于实现（打印机）特定。 |
| [set_FooterDistance](./set_footerdistance/)(double) | 用于设置 [Aspose::Words::PageSetup::get_FooterDistance](./get_footerdistance/). |
| [set_Gutter](./set_gutter/)(double) | 用于设置 [Aspose::Words::PageSetup::get_Gutter](./get_gutter/). |
| [set_HeaderDistance](./set_headerdistance/)(double) | 用于设置 [Aspose::Words::PageSetup::get_HeaderDistance](./get_headerdistance/). |
| [set_HeadingLevelForChapter](./set_headinglevelforchapter/)(int32_t) | 用于设置 [Aspose::Words::PageSetup::get_HeadingLevelForChapter](./get_headinglevelforchapter/). |
| [set_LayoutMode](./set_layoutmode/)(Aspose::Words::SectionLayoutMode) | 用于设置 [Aspose::Words::PageSetup::get_LayoutMode](./get_layoutmode/). |
| [set_LeftMargin](./set_leftmargin/)(double) | 用于设置 [Aspose::Words::PageSetup::get_LeftMargin](./get_leftmargin/). |
| [set_LineNumberCountBy](./set_linenumbercountby/)(int32_t) | 用于设置 [Aspose::Words::PageSetup::get_LineNumberCountBy](./get_linenumbercountby/). |
| [set_LineNumberDistanceFromText](./set_linenumberdistancefromtext/)(double) | 用于设置 [Aspose::Words::PageSetup::get_LineNumberDistanceFromText](./get_linenumberdistancefromtext/). |
| [set_LineNumberRestartMode](./set_linenumberrestartmode/)(Aspose::Words::LineNumberRestartMode) | 用于设置 [Aspose::Words::PageSetup::get_LineNumberRestartMode](./get_linenumberrestartmode/). |
| [set_LinesPerPage](./set_linesperpage/)(int32_t) | 用于设置 [Aspose::Words::PageSetup::get_LinesPerPage](./get_linesperpage/). |
| [set_LineStartingNumber](./set_linestartingnumber/)(int32_t) | 用于设置 [Aspose::Words::PageSetup::get_LineStartingNumber](./get_linestartingnumber/). |
| [set_Margins](./set_margins/)(Aspose::Words::Margins) | 用于设置 [Aspose::Words::PageSetup::get_Margins](./get_margins/). |
| [set_MultiplePages](./set_multiplepages/)(Aspose::Words::Settings::MultiplePagesType) | 用于设置 [Aspose::Words::PageSetup::get_MultiplePages](./get_multiplepages/). |
| [set_OddAndEvenPagesHeaderFooter](./set_oddandevenpagesheaderfooter/)(bool) | 用于设置 [Aspose::Words::PageSetup::get_OddAndEvenPagesHeaderFooter](./get_oddandevenpagesheaderfooter/). |
| [set_Orientation](./set_orientation/)(Aspose::Words::Orientation) | 用于设置 [Aspose::Words::PageSetup::get_Orientation](./get_orientation/)。 |
| [set_OtherPagesTray](./set_otherpagestray/)(int32_t) | 设置章节中除首页之外使用的纸盘（托盘）。该值取决于实现（打印机）特性。 |
| [set_PageHeight](./set_pageheight/)(double) | 用于设置 [Aspose::Words::PageSetup::get_PageHeight](./get_pageheight/)。 |
| [set_PageNumberStyle](./set_pagenumberstyle/)(Aspose::Words::NumberStyle) | 用于设置 [Aspose::Words::PageSetup::get_PageNumberStyle](./get_pagenumberstyle/)。 |
| [set_PageStartingNumber](./set_pagestartingnumber/)(int32_t) | 用于设置 [Aspose::Words::PageSetup::get_PageStartingNumber](./get_pagestartingnumber/)。 |
| [set_PageWidth](./set_pagewidth/)(double) | 用于设置 [Aspose::Words::PageSetup::get_PageWidth](./get_pagewidth/)。 |
| [set_PaperSize](./set_papersize/)(Aspose::Words::PaperSize) | 用于设置 [Aspose::Words::PageSetup::get_PaperSize](./get_papersize/)。 |
| [set_RestartPageNumbering](./set_restartpagenumbering/)(bool) | 用于设置 [Aspose::Words::PageSetup::get_RestartPageNumbering](./get_restartpagenumbering/)。 |
| [set_RightMargin](./set_rightmargin/)(double) | 用于设置 [Aspose::Words::PageSetup::get_RightMargin](./get_rightmargin/)。 |
| [set_RtlGutter](./set_rtlgutter/)(bool) | 用于设置 [Aspose::Words::PageSetup::get_RtlGutter](./get_rtlgutter/)。 |
| [set_SectionStart](./set_sectionstart/)(Aspose::Words::SectionStart) | 用于设置 [Aspose::Words::PageSetup::get_SectionStart](./get_sectionstart/)。 |
| [set_SheetsPerBooklet](./set_sheetsperbooklet/)(int32_t) | 用于设置 [Aspose::Words::PageSetup::get_SheetsPerBooklet](./get_sheetsperbooklet/)。 |
| [set_SuppressEndnotes](./set_suppressendnotes/)(bool) | 如果尾注打印在下一个未抑制尾注的章节末尾，则为 true。被抑制的尾注会在该章节的尾注之前打印。 |
| [set_TextOrientation](./set_textorientation/)(Aspose::Words::TextOrientation) | 用于设置 [Aspose::Words::PageSetup::get_TextOrientation](./get_textorientation/)。 |
| [set_TopMargin](./set_topmargin/)(double) | 用于设置 [Aspose::Words::PageSetup::get_TopMargin](./get_topmargin/)。 |
| [set_VerticalAlignment](./set_verticalalignment/)(Aspose::Words::PageVerticalAlignment) | 用于设置 [Aspose::Words::PageSetup::get_VerticalAlignment](./get_verticalalignment/)。 |
| static [Type](./type/)() |  |
## 备注


[PageSetup](./) object contains all the page setup attributes of a section (left margin, bottom margin, paper size, and so on) as properties.

## 示例



展示如何对文档中的节应用和恢复页面设置。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 修改构建器当前节的页面设置属性并添加文本。
builder->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
builder->get_PageSetup()->set_VerticalAlignment(Aspose::Words::PageVerticalAlignment::Center);
builder->Writeln(u"This is the first section, which landscape oriented with vertically centered text.");

// 如果我们使用文档构建器开始新节，
// 它将继承构建器当前的页面设置属性。
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

ASSERT_EQ(Aspose::Words::Orientation::Landscape, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_Orientation());
ASSERT_EQ(Aspose::Words::PageVerticalAlignment::Center, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_VerticalAlignment());

// 我们可以使用 "ClearFormatting" 方法将其页面设置属性恢复为默认值。
builder->get_PageSetup()->ClearFormatting();

ASSERT_EQ(Aspose::Words::Orientation::Portrait, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_Orientation());
ASSERT_EQ(Aspose::Words::PageVerticalAlignment::Top, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_VerticalAlignment());

builder->Writeln(u"This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc->Save(get_ArtifactsDir() + u"PageSetup.ClearFormatting.docx");
```

## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
