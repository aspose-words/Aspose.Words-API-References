---
title: "Aspose::Words::TableStyle class"
linktitle: "TableStyle"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::TableStyle 类。表示表格样式。欲了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 67000
url: /zh/cpp/aspose.words/tablestyle/
---
## TableStyle class


表示表格样式。要了解更多，请访问 [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/) 文档文章。

```cpp
class TableStyle : public Aspose::Words::Style,
                   public Aspose::Words::ICellAttrSource,
                   public Aspose::Words::IRowAttrSource,
                   public Aspose::Words::IBorderAttrSource,
                   public Aspose::Words::IShadingAttrSource
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Equals](../style/equals/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | 与指定的样式进行比较。仅比较内置样式的 Styles Istds。默认样式不包含在比较中。基样式、链接样式和下一段落样式会递归比较。 |
| [get_Aliases](../style/get_aliases/)() | 获取此样式的所有别名。如果样式没有别名，则返回空字符串数组。 |
| [get_Alignment](./get_alignment/)() | 指定表格样式的对齐方式。 |
| [get_AllowBreakAcrossPages](./get_allowbreakacrosspages/)() | 获取或设置一个标志，指示表格行中的文本是否允许跨页断开。 |
| [get_AutomaticallyUpdate](../style/get_automaticallyupdate/)() const | 指定此样式是否根据相应的值自动重新定义。 |
| [get_BaseStyleName](../style/get_basestylename/)() | 获取/设置此样式所基于的样式名称。 |
| [get_Borders](./get_borders/)() | 获取样式的默认单元格边框集合。 |
| [get_BottomPadding](./get_bottompadding/)() | 获取或设置在表格单元格内容下方添加的空间量（以点为单位）。 |
| [get_BuiltIn](../style/get_builtin/)() | 如果此样式是 MS Word 中的内置样式之一，则为 True。 |
| [get_CellSpacing](./get_cellspacing/)() | 获取或设置单元格之间的间距（以点为单位）。 |
| [get_ColumnStripe](./get_columnstripe/)() | 获取或设置在样式指定奇偶列分段时要包含在分段中的列数。 |
| [get_ConditionalStyles](./get_conditionalstyles/)() | 此表格样式可能定义的条件样式集合。 |
| [get_Document](../style/get_document/)() | 获取所属文档。 |
| [get_Font](../style/get_font/)() | 获取该样式的字符格式。 |
| [get_IsHeading](../style/get_isheading/)() | 当样式是内置标题样式之一时，为 True。 |
| [get_IsQuickStyle](../style/get_isquickstyle/)() const | 指定此样式是否显示在 MS Word UI 中的快速 [Style](../style/) 画廊。 |
| [get_LeftIndent](./get_leftindent/)() | 获取或设置表示表格左缩进的值。 |
| [get_LeftPadding](./get_leftpadding/)() | 获取或设置在表格单元格内容左侧添加的空间量（以点为单位）。 |
| [get_LinkedStyleName](../style/get_linkedstylename/)() | 获取/设置链接到此样式的 [Style](../style/) 名称。如果没有链接的样式，则返回空字符串。 |
| [get_List](../style/get_list/)() | 获取定义此列表样式格式的列表。 |
| [get_ListFormat](../style/get_listformat/)() | 提供对段落样式的列表格式属性的访问。 |
| [get_Locked](../style/get_locked/)() const | 指定此样式是否被锁定。 |
| [get_Name](../style/get_name/)() const | 获取或设置样式的名称。 |
| [get_NextParagraphStyleName](../style/get_nextparagraphstylename/)() | 获取/设置在使用指定样式格式化的段落后插入的新段落自动应用的样式名称。 |
| [get_ParagraphFormat](../style/get_paragraphformat/)() | 获取该样式的段落格式。 |
| [get_Priority](../style/get_priority/)() const | 获取/设置表示在“样式”任务窗格中对样式排序优先级的整数值。 |
| [get_RightPadding](./get_rightpadding/)() | 获取或设置在表格单元格内容右侧添加的空间量（以点为单位）。 |
| [get_RowStripe](./get_rowstripe/)() | 获取或设置在样式指定奇偶行分带时要包含的行数。 |
| [get_SemiHidden](../style/get_semihidden/)() const | 获取/设置样式是否从“样式”画廊和“样式”任务窗格中隐藏。 |
| [get_Shading](./get_shading/)() | 获取一个指向表格单元格阴影格式的 [Shading](../shading/) 对象。 |
| [get_StyleIdentifier](../style/get_styleidentifier/)() const | 获取内置样式的区域无关标识符。 |
| [get_Styles](../style/get_styles/)() const | 获取此样式所属的样式集合。 |
| [get_TopPadding](./get_toppadding/)() | 获取或设置在表格单元格内容上方添加的空间量（以点为单位）。 |
| [get_Type](../style/get_type/)() const | 获取样式类型（段落或字符）。 |
| [get_UnhideWhenUsed](../style/get_unhidewhenused/)() const | 获取/设置当前文档中使用的样式是否从“样式”画廊和“样式”任务窗格中取消隐藏。当使用的样式应显示在“样式”画廊中时，为 True。 |
| [get_VerticalAlignment](./get_verticalalignment/)() | 指定单元格的垂直对齐方式。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../style/remove/)() | 从文档中移除指定的样式。 |
| [set_Alignment](./set_alignment/)(Aspose::Words::Tables::TableAlignment) | 用于设置 [Aspose::Words::TableStyle::get_Alignment](./get_alignment/) 的 setter。 |
| [set_AllowBreakAcrossPages](./set_allowbreakacrosspages/)(bool) | 用于设置 [Aspose::Words::TableStyle::get_AllowBreakAcrossPages](./get_allowbreakacrosspages/) 的 setter。 |
| [set_AutomaticallyUpdate](../style/set_automaticallyupdate/)(bool) | 用于设置 [Aspose::Words::Style::get_AutomaticallyUpdate](../style/get_automaticallyupdate/) 的 setter。 |
| [set_BaseStyleName](../style/set_basestylename/)(const System::String\&) | 用于设置 [Aspose::Words::Style::get_BaseStyleName](../style/get_basestylename/) 的 setter。 |
| [set_BottomPadding](./set_bottompadding/)(double) | 用于设置 [Aspose::Words::TableStyle::get_BottomPadding](./get_bottompadding/) 的 setter。 |
| [set_CellSpacing](./set_cellspacing/)(double) | 用于设置 [Aspose::Words::TableStyle::get_CellSpacing](./get_cellspacing/) 的 setter。 |
| [set_ColumnStripe](./set_columnstripe/)(int32_t) | 用于设置 [Aspose::Words::TableStyle::get_ColumnStripe](./get_columnstripe/) 的 setter。 |
| [set_IsQuickStyle](../style/set_isquickstyle/)(bool) | 用于设置 [Aspose::Words::Style::get_IsQuickStyle](../style/get_isquickstyle/) 的 setter。 |
| [set_LeftIndent](./set_leftindent/)(double) | 用于设置 [Aspose::Words::TableStyle::get_LeftIndent](./get_leftindent/) 的 setter。 |
| [set_LeftPadding](./set_leftpadding/)(double) | 用于设置 [Aspose::Words::TableStyle::get_LeftPadding](./get_leftpadding/) 的 setter。 |
| [set_LinkedStyleName](../style/set_linkedstylename/)(const System::String\&) | 用于设置 [Aspose::Words::Style::get_LinkedStyleName](../style/get_linkedstylename/) 的 setter。 |
| [set_Locked](../style/set_locked/)(bool) | 用于设置 [Aspose::Words::Style::get_Locked](../style/get_locked/) 的 setter。 |
| [set_Name](../style/set_name/)(const System::String\&) | 用于设置 [Aspose::Words::Style::get_Name](../style/get_name/) 的 setter。 |
| [set_NextParagraphStyleName](../style/set_nextparagraphstylename/)(const System::String\&) | 用于设置 [Aspose::Words::Style::get_NextParagraphStyleName](../style/get_nextparagraphstylename/) 的 setter。 |
| [set_Priority](../style/set_priority/)(int32_t) | 用于设置 [Aspose::Words::Style::get_Priority](../style/get_priority/) 的 setter。 |
| [set_RightPadding](./set_rightpadding/)(double) | 用于设置 [Aspose::Words::TableStyle::get_RightPadding](./get_rightpadding/) 的 setter。 |
| [set_RowStripe](./set_rowstripe/)(int32_t) | 用于设置 [Aspose::Words::TableStyle::get_RowStripe](./get_rowstripe/) 的 setter。 |
| [set_SemiHidden](../style/set_semihidden/)(bool) | 用于设置 [Aspose::Words::Style::get_SemiHidden](../style/get_semihidden/) 的 setter。 |
| [set_TopPadding](./set_toppadding/)(double) | 用于设置 [Aspose::Words::TableStyle::get_TopPadding](./get_toppadding/) 的 setter。 |
| [set_UnhideWhenUsed](../style/set_unhidewhenused/)(bool) | 用于设置 [Aspose::Words::Style::get_UnhideWhenUsed](../style/get_unhidewhenused/) 的 setter。 |
| [set_VerticalAlignment](./set_verticalalignment/)(Aspose::Words::Tables::CellVerticalAlignment) | 用于设置 [Aspose::Words::TableStyle::get_VerticalAlignment](./get_verticalalignment/) 的 setter。 |
| static [Type](./type/)() |  |

## 示例



展示如何为表格创建自定义样式设置。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Name");
builder->InsertCell();
builder->Write(u"مرحبًا");
builder->EndRow();
builder->InsertCell();
builder->InsertCell();
builder->EndTable();

auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));
tableStyle->set_AllowBreakAcrossPages(true);
tableStyle->set_CellSpacing(5);
tableStyle->set_BottomPadding(20);
tableStyle->set_LeftPadding(5);
tableStyle->set_RightPadding(10);
tableStyle->set_TopPadding(20);
tableStyle->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_AntiqueWhite());
tableStyle->get_Borders()->set_Color(System::Drawing::Color::get_Blue());
tableStyle->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::DotDash);
tableStyle->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);

table->set_Style(tableStyle);

// 设置表格的样式属性可能会影响表格本身的属性。
ASSERT_FALSE(table->get_Bidi());
ASPOSE_ASSERT_EQ(5.0, table->get_CellSpacing());
ASSERT_EQ(u"MyTableStyle1", table->get_StyleName());

doc->Save(get_ArtifactsDir() + u"Table.TableStyleCreation.docx");
```

## 另见

* Class [Style](../style/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
