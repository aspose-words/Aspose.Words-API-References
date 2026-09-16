---
title: "Aspose::Words::Tables::Table 类"
linktitle: "表格"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::Table 类。表示 Word 文档中的表格。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words.tables/table/
---
## Table class


表示 Word 文档中的表格。要了解更多，请访问 [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/) 文档文章。

```cpp
class Table : public Aspose::Words::CompositeNode
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | 接受访问者。 |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | 接受访问者以访问表格的结束位置。 |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | 接受访问者以访问表格的起始位置。 |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [AutoFit](./autofit/)(Aspose::Words::Tables::AutoFitBehavior) | 根据指定的自动适应行为调整表格和单元格的大小。 |
| [ClearBorders](./clearborders/)() | 移除此表格上所有的表格和单元格边框。 |
| [ClearShading](./clearshading/)() | 移除表格上的所有底纹。 |
| [Clone](../../aspose.words/node/clone/)(bool) | 创建节点的副本。 |
| [ConvertToHorizontallyMergedCells](./converttohorizontallymergedcells/)() | 将按宽度水平合并的单元格转换为按 [HorizontalMerge](../cellformat/get_horizontalmerge/) 合并的单元格。 |
| [EnsureMinimum](./ensureminimum/)() | 如果表格没有行，则创建并追加一个 [Row](../row/)。 |
| [get_AbsoluteHorizontalDistance](./get_absolutehorizontaldistance/)() | 获取或设置由表格属性指定的绝对水平浮动表格位置，单位为点。默认值为 0。 |
| [get_AbsoluteVerticalDistance](./get_absoluteverticaldistance/)() | 获取或设置由表格属性指定的绝对垂直浮动表格位置，单位为点。默认值为 0。 |
| [get_Alignment](./get_alignment/)() | 指定内联表格在文档中的对齐方式。 |
| [get_AllowAutoFit](./get_allowautofit/)() | 允许 Microsoft Word 和 Aspose.Words 自动调整表格中单元格的大小以适应其内容。 |
| [get_AllowCellSpacing](./get_allowcellspacing/)() | 获取或设置 "Allow spacing between cells" 选项。 |
| [get_AllowOverlap](./get_allowoverlap/)() | 获取浮动表格在显示时是否允许文档中的其他浮动对象覆盖其范围。默认值为 **true**。 |
| [get_Bidi](./get_bidi/)() | 获取或设置此表格是否为从右到左的表格。 |
| [get_BottomPadding](./get_bottompadding/)() | 获取或设置在单元格内容下方添加的空间量（以磅为单位）。 |
| [get_CellSpacing](./get_cellspacing/)() | 获取或设置单元格之间的间距（以点为单位）。 |
| [get_Count](../../aspose.words/compositenode/get_count/)() | 获取此节点的直接子节点数量。 |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | 指定自定义节点标识符。 |
| [get_Description](./get_description/)() | 获取或设置此表格的描述。它提供表格中包含的信息的替代文本表示。 |
| [get_DistanceBottom](./get_distancebottom/)() | 获取或设置表格底部与周围文本之间的距离（以磅为单位）。 |
| [get_DistanceLeft](./get_distanceleft/)() | 获取或设置表格左侧与周围文本之间的距离（以磅为单位）。 |
| [get_DistanceRight](./get_distanceright/)() | 获取或设置表格右侧与周围文本之间的距离（以磅为单位）。 |
| [get_DistanceTop](./get_distancetop/)() | 获取或设置表格顶部与周围文本之间的距离（以磅为单位）。 |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | 获取此节点所属的文档。 |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | 获取节点的第一个子节点。 |
| [get_FirstRow](./get_firstrow/)() | 返回表格中的第一个 [Row](../row/) 节点。 |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | 如果此节点有任何子节点，则返回 **true**。 |
| [get_HorizontalAnchor](./get_horizontalanchor/)() | 获取应计算浮动表格水平定位的基对象。默认值为 [Column](../../aspose.words.drawing/relativehorizontalposition/)。 |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | 因为此节点可以拥有子节点，返回 **true**。 |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | 获取节点的最后一个子节点。 |
| [get_LastRow](./get_lastrow/)() | 返回表格中的最后一个 [Row](../row/) 节点。 |
| [get_LeftIndent](./get_leftindent/)() | 获取或设置表示表格左缩进的值。 |
| [get_LeftPadding](./get_leftpadding/)() | 获取或设置在单元格内容左侧添加的空间量（以磅为单位）。 |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | 获取紧随此节点之后的节点。 |
| [get_NodeType](./get_nodetype/)() const override | 返回 [Table](../../aspose.words/nodetype/)。 |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | 获取此节点的直接父节点。 |
| [get_PreferredWidth](./get_preferredwidth/)() | 获取或设置表格的首选宽度。 |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | 获取紧挨此节点之前的节点。 |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | 返回一个表示包含在此节点中的文档部分的 [Range](../../aspose.words/range/) 对象。 |
| [get_RelativeHorizontalAlignment](./get_relativehorizontalalignment/)() | 获取或设置浮动表格的相对水平对齐方式。 |
| [get_RelativeVerticalAlignment](./get_relativeverticalalignment/)() | 获取或设置浮动表格的相对垂直对齐方式。 |
| [get_RightPadding](./get_rightpadding/)() | 获取或设置在单元格内容右侧添加的空间量（以磅为单位）。 |
| [get_Rows](./get_rows/)() | 提供对表格行的强类型访问。 |
| [get_Style](./get_style/)() | 获取或设置应用于此表格的表格样式。 |
| [get_StyleIdentifier](./get_styleidentifier/)() | 获取或设置应用于此表格的表格样式的区域无关样式标识符。 |
| [get_StyleName](./get_stylename/)() | 获取或设置应用于此表格的表格样式的名称。 |
| [get_StyleOptions](./get_styleoptions/)() | 获取或设置指定表格样式如何应用于此表格的位标志。 |
| [get_TextWrapping](./get_textwrapping/)() | 获取或设置表格的 [TextWrapping](./get_textwrapping/)。 |
| [get_Title](./get_title/)() | 获取或设置此表格的标题。它提供了表格中包含的信息的替代文本表示。 |
| [get_TopPadding](./get_toppadding/)() | 获取或设置要在单元格内容上方添加的空间量（以点为单位）。 |
| [get_VerticalAnchor](./get_verticalanchor/)() | 获取用于计算浮动表格垂直定位的基对象。默认值为 [Margin](../../aspose.words.drawing/relativeverticalposition/)。 |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | 获取指定 [NodeType](../../aspose.words/nodetype/) 的第一个祖先节点。 |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | 返回匹配指定类型的第 N 个子节点。 |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | 返回匹配指定类型的子节点的实时集合。 |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | 提供对该节点的子节点进行 foreach 样式迭代的支持。 |
| [GetText](../../aspose.words/compositenode/gettext/)() override | 获取此节点及其所有子节点的文本。 |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../../aspose.words/compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 返回指定子节点在子节点数组中的索引。 |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 根据先序树遍历算法获取下一个节点。 |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | 一个将节点类型枚举值转换为用户友好字符串的实用方法。 |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 根据先序树遍历算法获取上一个节点。 |
| [Remove](../../aspose.words/node/remove/)() | 从父节点中移除自身。 |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | 移除当前节点的所有子节点。 |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | 移除当前节点的所有 [SmartTag](../../aspose.words.markup/smarttag/) 后代节点。 |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(const System::String\&) | 选择匹配 XPath 表达式的节点列表。 |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(const System::String\&) | 选择第一个匹配 XPath 表达式的 [Node](../../aspose.words/node/)。 |
| [set_AbsoluteHorizontalDistance](./set_absolutehorizontaldistance/)(double) | 用于设置 [Aspose::Words::Tables::Table::get_AbsoluteHorizontalDistance](./get_absolutehorizontaldistance/) 的 setter。 |
| [set_AbsoluteVerticalDistance](./set_absoluteverticaldistance/)(double) | 用于设置 [Aspose::Words::Tables::Table::get_AbsoluteVerticalDistance](./get_absoluteverticaldistance/) 的 setter。 |
| [set_Alignment](./set_alignment/)(Aspose::Words::Tables::TableAlignment) | 用于设置 [Aspose::Words::Tables::Table::get_Alignment](./get_alignment/) 的 setter。 |
| [set_AllowAutoFit](./set_allowautofit/)(bool) | 用于设置 [Aspose::Words::Tables::Table::get_AllowAutoFit](./get_allowautofit/) 的 setter。 |
| [set_AllowCellSpacing](./set_allowcellspacing/)(bool) | 用于设置 [Aspose::Words::Tables::Table::get_AllowCellSpacing](./get_allowcellspacing/) 的 setter。 |
| [set_Bidi](./set_bidi/)(bool) | 用于设置 [Aspose::Words::Tables::Table::get_Bidi](./get_bidi/) 的 setter。 |
| [set_BottomPadding](./set_bottompadding/)(double) | 用于设置 [Aspose::Words::Tables::Table::get_BottomPadding](./get_bottompadding/) 的 setter。 |
| [set_CellSpacing](./set_cellspacing/)(double) | 用于设置 [Aspose::Words::Tables::Table::get_CellSpacing](./get_cellspacing/) 的 setter。 |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | 用于设置 [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/) 的 setter。 |
| [set_Description](./set_description/)(const System::String\&) | 用于设置 [Aspose::Words::Tables::Table::get_Description](./get_description/) 的 setter。 |
| [set_DistanceBottom](./set_distancebottom/)(double) | 用于设置 [Aspose::Words::Tables::Table::get_DistanceBottom](./get_distancebottom/) 的 setter。 |
| [set_DistanceLeft](./set_distanceleft/)(double) | 用于设置 [Aspose::Words::Tables::Table::get_DistanceLeft](./get_distanceleft/) 的 setter。 |
| [set_DistanceRight](./set_distanceright/)(double) | 用于设置 [Aspose::Words::Tables::Table::get_DistanceRight](./get_distanceright/) 的 setter。 |
| [set_DistanceTop](./set_distancetop/)(double) | 用于设置 [Aspose::Words::Tables::Table::get_DistanceTop](./get_distancetop/) 的 setter。 |
| [set_HorizontalAnchor](./set_horizontalanchor/)(Aspose::Words::Drawing::RelativeHorizontalPosition) | 用于设置 [Aspose::Words::Tables::Table::get_HorizontalAnchor](./get_horizontalanchor/) 的 setter。 |
| [set_LeftIndent](./set_leftindent/)(double) | 用于设置 [Aspose::Words::Tables::Table::get_LeftIndent](./get_leftindent/) 的 setter。 |
| [set_LeftPadding](./set_leftpadding/)(double) | 用于设置 [Aspose::Words::Tables::Table::get_LeftPadding](./get_leftpadding/) 的 setter。 |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PreferredWidth](./set_preferredwidth/)(const System::SharedPtr\<Aspose::Words::Tables::PreferredWidth\>\&) | 用于设置 [Aspose::Words::Tables::Table::get_PreferredWidth](./get_preferredwidth/) 的 setter。 |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_RelativeHorizontalAlignment](./set_relativehorizontalalignment/)(Aspose::Words::Drawing::HorizontalAlignment) | 用于设置 [Aspose::Words::Tables::Table::get_RelativeHorizontalAlignment](./get_relativehorizontalalignment/) 的 setter。 |
| [set_RelativeVerticalAlignment](./set_relativeverticalalignment/)(Aspose::Words::Drawing::VerticalAlignment) | 用于设置 [Aspose::Words::Tables::Table::get_RelativeVerticalAlignment](./get_relativeverticalalignment/) 的 setter。 |
| [set_RightPadding](./set_rightpadding/)(double) | 用于设置 [Aspose::Words::Tables::Table::get_RightPadding](./get_rightpadding/) 的 setter。 |
| [set_Style](./set_style/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | 用于设置 [Aspose::Words::Tables::Table::get_Style](./get_style/) 的 setter。 |
| [set_StyleIdentifier](./set_styleidentifier/)(Aspose::Words::StyleIdentifier) | 用于 [Aspose::Words::Tables::Table::get_StyleIdentifier](./get_styleidentifier/) 的设置器。 |
| [set_StyleName](./set_stylename/)(const System::String\&) | 用于 [Aspose::Words::Tables::Table::get_StyleName](./get_stylename/) 的设置器。 |
| [set_StyleOptions](./set_styleoptions/)(Aspose::Words::Tables::TableStyleOptions) | 用于 [Aspose::Words::Tables::Table::get_StyleOptions](./get_styleoptions/) 的设置器。 |
| [set_TextWrapping](./set_textwrapping/)(Aspose::Words::Tables::TextWrapping) | 用于 [Aspose::Words::Tables::Table::get_TextWrapping](./get_textwrapping/) 的设置器。 |
| [set_Title](./set_title/)(const System::String\&) | 用于 [Aspose::Words::Tables::Table::get_Title](./get_title/) 的设置器。 |
| [set_TopPadding](./set_toppadding/)(double) | 用于 [Aspose::Words::Tables::Table::get_TopPadding](./get_toppadding/) 的设置器。 |
| [set_VerticalAnchor](./set_verticalanchor/)(Aspose::Words::Drawing::RelativeVerticalPosition) | 用于 [Aspose::Words::Tables::Table::get_VerticalAnchor](./get_verticalanchor/) 的设置器。 |
| [SetBorder](./setborder/)(Aspose::Words::BorderType, Aspose::Words::LineStyle, double, System::Drawing::Color, bool) | 将指定的表格边框设置为指定的线型、宽度和颜色。 |
| [SetBorders](./setborders/)(Aspose::Words::LineStyle, double, System::Drawing::Color) | 将所有表格边框设置为指定的线型、宽度和颜色。 |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetShading](./setshading/)(Aspose::Words::TextureIndex, System::Drawing::Color, System::Drawing::Color) | 将整个表格的阴影设置为指定的值。 |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [Table](./table/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) | 初始化 [Table](./) 类的新实例。 |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | 以指定格式将节点内容导出为字符串。 |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | 使用指定的保存选项将节点内容导出为字符串。 |
| static [Type](./type/)() |  |
## 备注


[Table](./) is a block-level node and can be a child of classes derived from [Story](../../aspose.words/story/) or [InlineStory](../../aspose.words/inlinestory/).

[Table](./) can contain one or more [Row](../row/) nodes.

一个最小的有效表格至少需要包含一个 [Row](../row/)。

## 示例



展示如何构建一个格式化的 2x2 表格。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->get_CellFormat()->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);
builder->Write(u"Row 1, cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, cell 2.");
builder->EndRow();

// 在构建表格时，文档生成器将把其当前的 RowFormat/CellFormat 属性值应用于
// 光标所在的当前行/单元格以及在创建时的任何新行/单元格。
ASSERT_EQ(Aspose::Words::Tables::CellVerticalAlignment::Center, table->get_Rows()->idx_get(0)->get_Cells()->idx_get(0)->get_CellFormat()->get_VerticalAlignment());
ASSERT_EQ(Aspose::Words::Tables::CellVerticalAlignment::Center, table->get_Rows()->idx_get(0)->get_Cells()->idx_get(1)->get_CellFormat()->get_VerticalAlignment());

builder->InsertCell();
builder->get_RowFormat()->set_Height(100);
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Exactly);
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Upward);
builder->Write(u"Row 2, cell 1.");
builder->InsertCell();
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Downward);
builder->Write(u"Row 2, cell 2.");
builder->EndRow();
builder->EndTable();

// 先前添加的行和单元格不会因构建器格式的更改而被追溯影响。
ASPOSE_ASSERT_EQ(0, table->get_Rows()->idx_get(0)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Auto, table->get_Rows()->idx_get(0)->get_RowFormat()->get_HeightRule());
ASPOSE_ASSERT_EQ(100, table->get_Rows()->idx_get(1)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Exactly, table->get_Rows()->idx_get(1)->get_RowFormat()->get_HeightRule());
ASSERT_EQ(Aspose::Words::TextOrientation::Upward, table->get_Rows()->idx_get(1)->get_Cells()->idx_get(0)->get_CellFormat()->get_Orientation());
ASSERT_EQ(Aspose::Words::TextOrientation::Downward, table->get_Rows()->idx_get(1)->get_Cells()->idx_get(1)->get_CellFormat()->get_Orientation());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.BuildTable.docx");
```


展示如何创建表格。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);

// 表格包含行，行包含单元格，单元格可能包含段落
// 以及诸如运行、形状，甚至其他表格等典型元素。
// 在表格上调用 "EnsureMinimum" 方法将确保
// 表格至少有一个行、单元格和段落。
auto firstRow = System::MakeObject<Aspose::Words::Tables::Row>(doc);
table->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(firstRow);

auto firstCell = System::MakeObject<Aspose::Words::Tables::Cell>(doc);
firstRow->AppendChild<System::SharedPtr<Aspose::Words::Tables::Cell>>(firstCell);

auto paragraph = System::MakeObject<Aspose::Words::Paragraph>(doc);
firstCell->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(paragraph);

// 向表格的第一行第一列单元格添加文本。
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->Save(get_ArtifactsDir() + u"Table.CreateTable.docx");
```


展示如何遍历文档中的所有表格并打印每个单元格的内容。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::TableCollection> tables = doc->get_FirstSection()->get_Body()->get_Tables();

ASSERT_EQ(2, tables->ToArray()->get_Length());

for (int32_t i = 0; i < tables->get_Count(); i++)
{
    std::cout << System::String::Format(u"Start of Table {0}", i) << std::endl;

    System::SharedPtr<Aspose::Words::Tables::RowCollection> rows = tables->idx_get(i)->get_Rows();

    // 我们可以在行集合上使用 "ToArray" 方法将其克隆为数组。
    ASPOSE_ASSERT_EQ(rows, rows->ToArray());
    ASPOSE_ASSERT_NS(rows, rows->ToArray());

    for (int32_t j = 0; j < rows->get_Count(); j++)
    {
        std::cout << System::String::Format(u"\tStart of Row {0}", j) << std::endl;

        System::SharedPtr<Aspose::Words::Tables::CellCollection> cells = rows->idx_get(j)->get_Cells();

        // 我们可以在单元格集合上使用 "ToArray" 方法将其克隆为数组。
        ASPOSE_ASSERT_EQ(cells, cells->ToArray());
        ASPOSE_ASSERT_NS(cells, cells->ToArray());

        for (int32_t k = 0; k < cells->get_Count(); k++)
        {
            System::String cellText = cells->idx_get(k)->ToString(Aspose::Words::SaveFormat::Text).Trim();
            std::cout << System::String::Format(u"\t\tContents of Cell:{0} = \"{1}\"", k, cellText) << std::endl;
        }

        std::cout << System::String::Format(u"\tEnd of Row {0}", j) << std::endl;
    }

    std::cout << System::String::Format(u"End of Table {0}\n", i) << std::endl;
}
```

## 另见

* Class [CompositeNode](../../aspose.words/compositenode/)
* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
