---
title: "Aspose::Words::ParagraphFormat class"
linktitle: "ParagraphFormat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ParagraphFormat 类。表示段落的所有格式设置。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 49000
url: /zh/cpp/aspose.words/paragraphformat/
---
## ParagraphFormat class


表示段落的所有格式设置。要了解更多，请访问 [Working with Paragraphs](https://docs.aspose.com/words/cpp/working-with-paragraphs/) 文档文章。

```cpp
class ParagraphFormat : public Aspose::Words::IBorderAttrSource,
                        public Aspose::Words::IShadingAttrSource
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | 重置为默认段落格式。 |
| [get_AddSpaceBetweenFarEastAndAlpha](./get_addspacebetweenfareastandalpha/)() | 获取或设置一个标志，指示是否在当前段落的拉丁文本区域和东亚文本区域之间自动调整字符间距。 |
| [get_AddSpaceBetweenFarEastAndDigit](./get_addspacebetweenfareastanddigit/)() | 获取或设置一个标志，指示是否在当前段落的数字区域和东亚文本区域之间自动调整字符间距。 |
| [get_Alignment](./get_alignment/)() | 获取或设置段落的文本对齐方式。 |
| [get_BaselineAlignment](./get_baselinealignment/)() | 获取或设置字体在行上的垂直位置。 |
| [get_Bidi](./get_bidi/)() | 获取或设置此段落是否为从右到左。 |
| [get_Borders](./get_borders/)() | 获取段落的边框集合。 |
| [get_CharacterUnitFirstLineIndent](./get_characterunitfirstlineindent/)() | 获取或设置首行缩进或悬挂缩进的值（以字符为单位）。使用正值设置首行缩进，使用负值设置悬挂缩进。 |
| [get_CharacterUnitLeftIndent](./get_characterunitleftindent/)() | 获取或设置指定段落的左缩进值（以字符为单位）。 |
| [get_CharacterUnitRightIndent](./get_characterunitrightindent/)() | 获取或设置指定段落的右缩进值（以字符为单位）。 |
| [get_DropCapPosition](./get_dropcapposition/)() | 获取或设置首字下沉文本的位置。 |
| [get_FarEastLineBreakControl](./get_fareastlinebreakcontrol/)() | 获取或设置一个标志，指示是否对当前段落应用东亚换行规则。 |
| [get_FirstLineIndent](./get_firstlineindent/)() | 获取或设置首行或悬挂缩进的值（以磅为单位）。使用正值设置首行缩进，使用负值设置悬挂缩进。 |
| [get_HangingPunctuation](./get_hangingpunctuation/)() | 获取或设置一个标志，指示当前段落是否启用悬挂标点。 |
| [get_IsHeading](./get_isheading/)() | 当段落样式是内置标题样式之一时为 true。 |
| [get_IsListItem](./get_islistitem/)() | 当段落是项目符号或编号列表中的项目时为 True。 |
| [get_KeepTogether](./get_keeptogether/)() | 如果段落中的所有行必须保持在同一页上，则为 True。 |
| [get_KeepWithNext](./get_keepwithnext/)() | 如果段落应与其后面的段落保持在同一页上，则为 True。 |
| [get_LeftIndent](./get_leftindent/)() | 获取或设置表示段落左缩进的值（以点为单位）。 |
| [get_LineSpacing](./get_linespacing/)() | 获取或设置段落的行距（以点为单位）。 |
| [get_LineSpacingRule](./get_linespacingrule/)() | 获取或设置段落的行距。 |
| [get_LinesToDrop](./get_linestodrop/)() | 获取或设置用于计算首字母放大高度的段落文本行数。 |
| [get_LineUnitAfter](./get_lineunitafter/)() | 获取或设置段落之后的间距量（以网格线为单位）。 |
| [get_LineUnitBefore](./get_lineunitbefore/)() | 获取或设置段落之前的间距量（以网格线为单位）。 |
| [get_MirrorIndents](./get_mirrorindents/)() | 获取或设置指示左、右缩进是否具有相同宽度的标志。 |
| [get_NoSpaceBetweenParagraphsOfSameStyle](./get_nospacebetweenparagraphsofsamestyle/)() | 当 **true** 时，同一样式的段落之间的 [SpaceBefore](./get_spacebefore/) 和 [SpaceAfter](./get_spaceafter/) 将被忽略。 |
| [get_OutlineLevel](./get_outlinelevel/)() | 指定段落在文档中的大纲级别。 |
| [get_PageBreakBefore](./get_pagebreakbefore/)() | 如果在段落前强制换页，则为 True。 |
| [get_RightIndent](./get_rightindent/)() | 获取或设置表示段落右缩进的值（以点为单位）。 |
| [get_Shading](./get_shading/)() | 返回一个指向段落阴影格式的 [Shading](../shading/) 对象。 |
| [get_SnapToGrid](./get_snaptogrid/)() | 指定当前段落在布局内容时是否应使用文档每页网格线设置。 |
| [get_SpaceAfter](./get_spaceafter/)() | 获取或设置段落之后的间距量（以点为单位）。 |
| [get_SpaceAfterAuto](./get_spaceafterauto/)() | 如果段落之后的间距量是自动设置的，则为 True。 |
| [get_SpaceBefore](./get_spacebefore/)() | 获取或设置段落之前的间距量（以点为单位）。 |
| [get_SpaceBeforeAuto](./get_spacebeforeauto/)() | 如果段落之前的间距量是自动设置的，则为 True。 |
| [get_Style](./get_style/)() | 获取或设置应用于此格式的段落样式。 |
| [get_StyleIdentifier](./get_styleidentifier/)() | 获取或设置应用于此格式的段落样式的与区域无关的样式标识符。 |
| [get_StyleName](./get_stylename/)() | 获取或设置应用于此格式的段落样式的名称。 |
| [get_SuppressAutoHyphens](./get_suppressautohyphens/)() | 指定当前段落是否应免除文档设置中应用的任何连字符处理。 |
| [get_SuppressLineNumbers](./get_suppresslinenumbers/)() | 指定当前段落的行是否应免除在父节中应用的行号编号。 |
| [get_TabStops](./get_tabstops/)() | 获取为此对象定义的自定义制表位集合。 |
| [get_WidowControl](./get_widowcontrol/)() | 如果段落的第一行和最后一行应与段落其余部分保持在同一页，则为 True。 |
| [get_WordWrap](./get_wordwrap/)() | 如果此属性为 **false**，则当前段落中单词中间的拉丁文本可以换行。否则，拉丁文本将按完整单词换行。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AddSpaceBetweenFarEastAndAlpha](./set_addspacebetweenfareastandalpha/)(bool) | 用于设置 [Aspose::Words::ParagraphFormat::get_AddSpaceBetweenFarEastAndAlpha](./get_addspacebetweenfareastandalpha/)。 |
| [set_AddSpaceBetweenFarEastAndDigit](./set_addspacebetweenfareastanddigit/)(bool) | 用于设置 [Aspose::Words::ParagraphFormat::get_AddSpaceBetweenFarEastAndDigit](./get_addspacebetweenfareastanddigit/)。 |
| [set_Alignment](./set_alignment/)(Aspose::Words::ParagraphAlignment) | 用于设置 [Aspose::Words::ParagraphFormat::get_Alignment](./get_alignment/)。 |
| [set_BaselineAlignment](./set_baselinealignment/)(Aspose::Words::BaselineAlignment) | 用于设置 [Aspose::Words::ParagraphFormat::get_BaselineAlignment](./get_baselinealignment/)。 |
| [set_Bidi](./set_bidi/)(bool) | 用于设置 [Aspose::Words::ParagraphFormat::get_Bidi](./get_bidi/)。 |
| [set_CharacterUnitFirstLineIndent](./set_characterunitfirstlineindent/)(double) | 用于设置 [Aspose::Words::ParagraphFormat::get_CharacterUnitFirstLineIndent](./get_characterunitfirstlineindent/)。 |
| [set_CharacterUnitLeftIndent](./set_characterunitleftindent/)(double) | 用于设置 [Aspose::Words::ParagraphFormat::get_CharacterUnitLeftIndent](./get_characterunitleftindent/)。 |
| [set_CharacterUnitRightIndent](./set_characterunitrightindent/)(double) | 用于设置 [Aspose::Words::ParagraphFormat::get_CharacterUnitRightIndent](./get_characterunitrightindent/)。 |
| [set_DropCapPosition](./set_dropcapposition/)(Aspose::Words::DropCapPosition) | 用于设置 [Aspose::Words::ParagraphFormat::get_DropCapPosition](./get_dropcapposition/)。 |
| [set_FarEastLineBreakControl](./set_fareastlinebreakcontrol/)(bool) | 用于设置 [Aspose::Words::ParagraphFormat::get_FarEastLineBreakControl](./get_fareastlinebreakcontrol/)。 |
| [set_FirstLineIndent](./set_firstlineindent/)(double) | 用于设置 [Aspose::Words::ParagraphFormat::get_FirstLineIndent](./get_firstlineindent/)。 |
| [set_HangingPunctuation](./set_hangingpunctuation/)(bool) | 用于设置 [Aspose::Words::ParagraphFormat::get_HangingPunctuation](./get_hangingpunctuation/)。 |
| [set_KeepTogether](./set_keeptogether/)(bool) | 用于设置 [Aspose::Words::ParagraphFormat::get_KeepTogether](./get_keeptogether/)。 |
| [set_KeepWithNext](./set_keepwithnext/)(bool) | 用于设置 [Aspose::Words::ParagraphFormat::get_KeepWithNext](./get_keepwithnext/)。 |
| [set_LeftIndent](./set_leftindent/)(double) | 用于设置 [Aspose::Words::ParagraphFormat::get_LeftIndent](./get_leftindent/)。 |
| [set_LineSpacing](./set_linespacing/)(double) | 用于设置 [Aspose::Words::ParagraphFormat::get_LineSpacing](./get_linespacing/)。 |
| [set_LineSpacingRule](./set_linespacingrule/)(Aspose::Words::LineSpacingRule) | 用于设置 [Aspose::Words::ParagraphFormat::get_LineSpacingRule](./get_linespacingrule/)。 |
| [set_LinesToDrop](./set_linestodrop/)(int32_t) | 用于设置 [Aspose::Words::ParagraphFormat::get_LinesToDrop](./get_linestodrop/)。 |
| [set_LineUnitAfter](./set_lineunitafter/)(double) | 用于设置 [Aspose::Words::ParagraphFormat::get_LineUnitAfter](./get_lineunitafter/)。 |
| [set_LineUnitBefore](./set_lineunitbefore/)(double) | 用于设置 [Aspose::Words::ParagraphFormat::get_LineUnitBefore](./get_lineunitbefore/)。 |
| [set_MirrorIndents](./set_mirrorindents/)(bool) | 用于设置 [Aspose::Words::ParagraphFormat::get_MirrorIndents](./get_mirrorindents/)。 |
| [set_NoSpaceBetweenParagraphsOfSameStyle](./set_nospacebetweenparagraphsofsamestyle/)(bool) | 用于设置 [Aspose::Words::ParagraphFormat::get_NoSpaceBetweenParagraphsOfSameStyle](./get_nospacebetweenparagraphsofsamestyle/)。 |
| [set_OutlineLevel](./set_outlinelevel/)(Aspose::Words::OutlineLevel) | 用于设置 [Aspose::Words::ParagraphFormat::get_OutlineLevel](./get_outlinelevel/) 的 setter。 |
| [set_PageBreakBefore](./set_pagebreakbefore/)(bool) | 用于设置 [Aspose::Words::ParagraphFormat::get_PageBreakBefore](./get_pagebreakbefore/) 的 setter。 |
| [set_RightIndent](./set_rightindent/)(double) | 用于设置 [Aspose::Words::ParagraphFormat::get_RightIndent](./get_rightindent/) 的 setter。 |
| [set_SnapToGrid](./set_snaptogrid/)(bool) | 用于设置 [Aspose::Words::ParagraphFormat::get_SnapToGrid](./get_snaptogrid/) 的 setter。 |
| [set_SpaceAfter](./set_spaceafter/)(double) | 用于设置 [Aspose::Words::ParagraphFormat::get_SpaceAfter](./get_spaceafter/) 的 setter。 |
| [set_SpaceAfterAuto](./set_spaceafterauto/)(bool) | 用于设置 [Aspose::Words::ParagraphFormat::get_SpaceAfterAuto](./get_spaceafterauto/) 的 setter。 |
| [set_SpaceBefore](./set_spacebefore/)(double) | 用于设置 [Aspose::Words::ParagraphFormat::get_SpaceBefore](./get_spacebefore/) 的 setter。 |
| [set_SpaceBeforeAuto](./set_spacebeforeauto/)(bool) | 用于设置 [Aspose::Words::ParagraphFormat::get_SpaceBeforeAuto](./get_spacebeforeauto/) 的 setter。 |
| [set_Style](./set_style/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | 用于设置 [Aspose::Words::ParagraphFormat::get_Style](./get_style/) 的 setter。 |
| [set_StyleIdentifier](./set_styleidentifier/)(Aspose::Words::StyleIdentifier) | 用于设置 [Aspose::Words::ParagraphFormat::get_StyleIdentifier](./get_styleidentifier/) 的 setter。 |
| [set_StyleName](./set_stylename/)(const System::String\&) | 用于设置 [Aspose::Words::ParagraphFormat::get_StyleName](./get_stylename/) 的 setter。 |
| [set_SuppressAutoHyphens](./set_suppressautohyphens/)(bool) | 用于设置 [Aspose::Words::ParagraphFormat::get_SuppressAutoHyphens](./get_suppressautohyphens/) 的 setter。 |
| [set_SuppressLineNumbers](./set_suppresslinenumbers/)(bool) | 用于设置 [Aspose::Words::ParagraphFormat::get_SuppressLineNumbers](./get_suppresslinenumbers/) 的 setter。 |
| [set_WidowControl](./set_widowcontrol/)(bool) | 用于设置 [Aspose::Words::ParagraphFormat::get_WidowControl](./get_widowcontrol/) 的 setter。 |
| [set_WordWrap](./set_wordwrap/)(bool) | 用于设置 [Aspose::Words::ParagraphFormat::get_WordWrap](./get_wordwrap/) 的 setter。 |
| static [Type](./type/)() |  |

## 示例



展示如何手动构建 Aspose.Words 文档。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 空白文档包含一个节、一个主体和一个段落。
// 调用 "RemoveAllChildren" 方法以删除所有这些节点，
// 最终得到一个没有子节点的文档节点。
doc->RemoveAllChildren();

// 此文档现在没有可用于添加内容的复合子节点。
// 如果我们想编辑它，需要重新填充其节点集合。
// 首先，创建一个新节，然后将其作为子节点追加到根文档节点。
auto section = System::MakeObject<Aspose::Words::Section>(doc);
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(section);

// 为该节设置一些页面布局属性。
section->get_PageSetup()->set_SectionStart(Aspose::Words::SectionStart::NewPage);
section->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Letter);

// 一个节需要一个主体，用于包含并显示其所有内容
// 在页面上位于该节的页眉和页脚之间。
auto body = System::MakeObject<Aspose::Words::Body>(doc);
section->AppendChild<System::SharedPtr<Aspose::Words::Body>>(body);

// 创建一个段落，设置一些格式属性，然后将其作为子节点追加到主体中。
auto para = System::MakeObject<Aspose::Words::Paragraph>(doc);

para->get_ParagraphFormat()->set_StyleName(u"Heading 1");
para->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

body->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(para);

// 最后，添加一些内容以完成文档。创建一个运行（run），
// 设置其外观和内容，然后将其作为子节点追加到段落中。
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"Hello World!");
run->get_Font()->set_Color(System::Drawing::Color::get_Red());
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

ASSERT_EQ(u"Hello World!", doc->GetText().Trim());

doc->Save(get_ArtifactsDir() + u"Section.CreateManually.docx");
```

## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
