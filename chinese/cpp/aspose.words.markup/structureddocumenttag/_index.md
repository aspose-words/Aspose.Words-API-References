---
title: "Aspose::Words::Markup::StructuredDocumentTag 类"
linktitle: "StructuredDocumentTag"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Markup::StructuredDocumentTag 类。表示文档中的结构化文档标签（SDT 或内容控件）。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 11000
url: /zh/cpp/aspose.words.markup/structureddocumenttag/
---
## StructuredDocumentTag class


表示文档中的结构化文档标签（SDT 或内容控件）。了解更多，请访问 [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/) 文档文章。

```cpp
class StructuredDocumentTag : public Aspose::Words::CompositeNode,
                              public Aspose::Words::Markup::IMarkupNode,
                              public Aspose::Words::Revisions::ITrackableNode,
                              public Aspose::Words::IRunAttrSource,
                              public Aspose::Words::Markup::IStructuredDocumentTag
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | 接受访问者。 |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | 接受访问者以访问 [StructuredDocumentTag](./) 的结束位置。 |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | 接受访问者以访问 [StructuredDocumentTag](./) 的起始位置。 |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clear](./clear/)() | 清除此结构化文档标签的内容，并在已定义时显示占位符。 |
| [Clone](../../aspose.words/node/clone/)(bool) | 创建节点的副本。 |
| [get_Appearance](./get_appearance/)() override | 获取/设置结构化文档标签的外观。 |
| [get_BuildingBlockCategory](./get_buildingblockcategory/)() | 指定此 **SDT** 节点的构建块类别。不能为空 **null**。 |
| [get_BuildingBlockGallery](./get_buildingblockgallery/)() | 指定此 **SDT** 的构建块类型。不能为空 **null**。 |
| [get_CalendarType](./get_calendartype/)() | 指定此 **SDT** 的日历类型。默认是 [Default](../sdtcalendartype/) |
| [get_Checked](./get_checked/)() | 获取/设置复选框 **SDT** 的当前状态。此属性的默认值为 **false**。 |
| [get_Color](./get_color/)() override | 获取或设置结构化文档标签的颜色。 |
| [get_ContentsFont](./get_contentsfont/)() | [Font](../../aspose.words/font/) 格式将应用于输入到 **SDT** 的文本。 |
| [get_Count](../../aspose.words/compositenode/get_count/)() | 获取此节点的直接子节点数量。 |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | 指定自定义节点标识符。 |
| [get_DateDisplayFormat](./get_datedisplayformat/)() | 表示日期显示格式的字符串。 |
| [get_DateDisplayLocale](./get_datedisplaylocale/)() | 允许设置/获取此 **SDT** 中显示的日期的语言格式。 |
| [get_DateStorageFormat](./get_datestorageformat/)() | 获取/设置当 **SDT** 绑定到文档数据存储中的 XML 节点时，日期 SDT 的日期存储格式。默认值为 [DateTime](../sdtdatestorageformat/) |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | 获取此节点所属的文档。 |
| [get_EndCharacterFont](./get_endcharacterfont/)() | [Font](../../aspose.words/font/) 格式将应用于输入到 **SDT** 的文本的最后一个字符。 |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | 获取节点的第一个子节点。 |
| [get_FullDate](./get_fulldate/)() | 指定最后输入到此 **SDT** 的完整日期和时间。 |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | 如果此节点有任何子节点，则返回 **true**。 |
| [get_Id](./get_id/)() override | 为此 **SDT** 指定唯一的只读持久数值 Id。 |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | 因为此节点可以拥有子节点，返回 **true**。 |
| [get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/)() override | 指定此 **SDT** 的内容是否应被解释为包含占位符文本（而不是 SDT 中的常规文本内容）。如果设置为 **true**，则在打开此文档时将恢复此状态（显示占位符文本）。 |
| [get_IsTemporary](./get_istemporary/)() const | 指定当其内容被修改时，是否应从 WordProcessingML 文档中移除此 **SDT**。 |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | 获取节点的最后一个子节点。 |
| [get_Level](./get_level/)() const override | 获取此 **SDT** 在文档树中出现的层级。 |
| [get_ListItems](./get_listitems/)() | 获取与此 **SDT** 关联的 [SdtListItemCollection](../sdtlistitemcollection/)。 |
| [get_LockContentControl](./get_lockcontentcontrol/)() override | 设置为 **true** 时，此属性将禁止用户删除此 **SDT**。 |
| [get_LockContents](./get_lockcontents/)() override | 设置为 **true** 时，此属性将禁止用户编辑此 **SDT** 的内容。 |
| [get_Multiline](./get_multiline/)() | 指定此 **SDT** 是否允许多行文本。 |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | 获取紧随此节点之后的节点。 |
| [get_NodeType](./get_nodetype/)() const override | 返回 [StructuredDocumentTag](../../aspose.words/nodetype/)。 |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | 获取此节点的直接父节点。 |
| [get_Placeholder](./get_placeholder/)() override | 获取包含占位符文本的 [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/)，当此 SDT 运行内容为空、通过 [XmlMapping](./get_xmlmapping/) 元素指定的关联映射 XML 元素为空，或 [IsShowingPlaceholderText](./get_isshowingplaceholdertext/) 元素为 **true** 时应显示该文本。 |
| [get_PlaceholderName](./get_placeholdername/)() override | 获取或设置包含占位符文本的 [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) 的名称。 |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | 获取紧挨此节点之前的节点。 |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | 返回一个表示包含在此节点中的文档部分的 [Range](../../aspose.words/range/) 对象。 |
| [get_SdtType](./get_sdttype/)() override | 获取此 **Structured document tag** 的类型。 |
| [get_Style](./get_style/)() | 获取或设置结构化文档标签的 [Style](../../aspose.words/style/)。 |
| [get_StyleName](./get_stylename/)() | 获取或设置应用于结构化文档标签的样式名称。 |
| [get_Tag](./get_tag/)() const override | 指定与当前 SDT 节点关联的标签。不能为空 **null**。 |
| [get_Title](./get_title/)() const override | 指定与此 **SDT** 关联的友好名称。不能为空 **null**。 |
| [get_WordOpenXML](./get_wordopenxml/)() override | 获取一个字符串，表示节点中以 [FlatOpc](../../aspose.words/saveformat/) 格式包含的 XML。 |
| [get_WordOpenXMLMinimal](./get_wordopenxmlminimal/)() | 获取一个字符串，表示以 [FlatOpc](../../aspose.words/saveformat/) 格式包含在节点内的 XML。与 [WordOpenXML](./get_wordopenxml/) 属性不同，此方法生成一个剥离了任何非内容相关部分的精简文档。 |
| [get_XmlMapping](./get_xmlmapping/)() override | 获取一个对象，表示此结构化文档标签映射到当前文档的自定义 XML 部分中的 XML 数据。 |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | 获取指定 [NodeType](../../aspose.words/nodetype/) 的第一个祖先节点。 |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | 返回匹配指定类型的第 N 个子节点。 |
| [GetChildNodes](./getchildnodes/)(Aspose::Words::NodeType, bool) override | 返回匹配指定类型的子节点的实时集合。 |
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
| [RemoveSelfOnly](./removeselfonly/)() override | 仅删除此 SDT 节点本身，但保留其内容在文档树中。 |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | 移除当前节点的所有 [SmartTag](../smarttag/) 子孙节点。 |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(const System::String\&) | 选择匹配 XPath 表达式的节点列表。 |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(const System::String\&) | 选择第一个匹配 XPath 表达式的 [Node](../../aspose.words/node/)。 |
| [set_Appearance](./set_appearance/)(Aspose::Words::Markup::SdtAppearance) override | [Aspose::Words::Markup::StructuredDocumentTag::get_Appearance](./get_appearance/) 的设置器。 |
| [set_BuildingBlockCategory](./set_buildingblockcategory/)(const System::String\&) | [Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockCategory](./get_buildingblockcategory/) 的设置器。 |
| [set_BuildingBlockGallery](./set_buildingblockgallery/)(const System::String\&) | [Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockGallery](./get_buildingblockgallery/) 的设置器。 |
| [set_CalendarType](./set_calendartype/)(Aspose::Words::Markup::SdtCalendarType) | 用于设置 [Aspose::Words::Markup::StructuredDocumentTag::get_CalendarType](./get_calendartype/)。 |
| [set_Checked](./set_checked/)(bool) | 用于设置 [Aspose::Words::Markup::StructuredDocumentTag::get_Checked](./get_checked/)。 |
| [set_Color](./set_color/)(System::Drawing::Color) override | 用于设置 [Aspose::Words::Markup::StructuredDocumentTag::get_Color](./get_color/)。 |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | 用于设置 [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/) 的 setter。 |
| [set_DateDisplayFormat](./set_datedisplayformat/)(const System::String\&) | 用于设置 [Aspose::Words::Markup::StructuredDocumentTag::get_DateDisplayFormat](./get_datedisplayformat/)。 |
| [set_DateDisplayLocale](./set_datedisplaylocale/)(int32_t) | 用于设置 [Aspose::Words::Markup::StructuredDocumentTag::get_DateDisplayLocale](./get_datedisplaylocale/)。 |
| [set_DateStorageFormat](./set_datestorageformat/)(Aspose::Words::Markup::SdtDateStorageFormat) | 用于设置 [Aspose::Words::Markup::StructuredDocumentTag::get_DateStorageFormat](./get_datestorageformat/)。 |
| [set_FullDate](./set_fulldate/)(System::DateTime) | 用于设置 [Aspose::Words::Markup::StructuredDocumentTag::get_FullDate](./get_fulldate/)。 |
| [set_IsShowingPlaceholderText](./set_isshowingplaceholdertext/)(bool) override | 用于设置 [Aspose::Words::Markup::StructuredDocumentTag::get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/)。 |
| [set_IsTemporary](./set_istemporary/)(bool) | 用于设置 [Aspose::Words::Markup::StructuredDocumentTag::get_IsTemporary](./get_istemporary/)。 |
| [set_LockContentControl](./set_lockcontentcontrol/)(bool) override | 用于设置 [Aspose::Words::Markup::StructuredDocumentTag::get_LockContentControl](./get_lockcontentcontrol/)。 |
| [set_LockContents](./set_lockcontents/)(bool) override | 用于设置 [Aspose::Words::Markup::StructuredDocumentTag::get_LockContents](./get_lockcontents/)。 |
| [set_Multiline](./set_multiline/)(bool) | 用于设置 [Aspose::Words::Markup::StructuredDocumentTag::get_Multiline](./get_multiline/)。 |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PlaceholderName](./set_placeholdername/)(System::String) override | 用于设置 [Aspose::Words::Markup::StructuredDocumentTag::get_PlaceholderName](./get_placeholdername/)。 |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_Style](./set_style/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | 用于设置 [Aspose::Words::Markup::StructuredDocumentTag::get_Style](./get_style/)。 |
| [set_StyleName](./set_stylename/)(const System::String\&) | 用于设置 [Aspose::Words::Markup::StructuredDocumentTag::get_StyleName](./get_stylename/)。 |
| [set_Tag](./set_tag/)(System::String) override | 用于设置 [Aspose::Words::Markup::StructuredDocumentTag::get_Tag](./get_tag/)。 |
| [set_Title](./set_title/)(System::String) override | 用于设置 [Aspose::Words::Markup::StructuredDocumentTag::get_Title](./get_title/)。 |
| [SetCheckedSymbol](./setcheckedsymbol/)(int32_t, const System::String\&) | 设置用于表示复选框内容控件已选状态的符号。 |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [SetUncheckedSymbol](./setuncheckedsymbol/)(int32_t, const System::String\&) | 设置用于表示复选框内容控件未选状态的符号。 |
| [StructuredDocumentTag](./structureddocumenttag/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::Markup::SdtType, Aspose::Words::Markup::MarkupLevel) | 初始化 **Structured document tag** 类的新实例。 |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | 以指定格式将节点内容导出为字符串。 |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | 使用指定的保存选项将节点内容导出为字符串。 |
| static [Type](./type/)() |  |
## 备注


结构化文档标签（SDT）允许将客户定义的语义以及其行为和外观嵌入文档中。

在此版本中，Aspose.Words 提供了许多公共方法和属性来操作 [StructuredDocumentTag](./) 的行为和内容。可以使用 [XmlMapping](./get_xmlmapping/) 属性将 SDT 节点映射到文档中的自定义 XML 包。

[StructuredDocumentTag](./) can occur in a document in the following places:

* Block-level - Among paragraphs and tables, as a child of a [Body](../../aspose.words/body/), [HeaderFooter](../../aspose.words/headerfooter/), [Comment](../../aspose.words/comment/), [Footnote](../../aspose.words.notes/footnote/) or a [Shape](../../aspose.words.drawing/shape/) node.
* Row-level - Among rows in a table, as a child of a [Table](../../aspose.words.tables/table/) node.
* Cell-level - Among cells in a table row, as a child of a [Row](../../aspose.words.tables/row/) node.
* Inline-level - Among inline content inside, as a child of a [Paragraph](../../aspose.words/paragraph/).
* Nested inside another [StructuredDocumentTag](./).



## 示例



展示如何使用内容控件元素的样式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 下面有两种方法将文档中的样式应用于结构化文档标签。
// 1 -  从文档的样式集合中应用样式对象：
System::SharedPtr<Aspose::Words::Style> quoteStyle = doc->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Quote);
auto sdtPlainText = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);
sdtPlainText->set_Style(quoteStyle);

// 2 -  按名称引用文档中的样式:
auto sdtRichText = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::RichText, Aspose::Words::Markup::MarkupLevel::Inline);
sdtRichText->set_StyleName(u"Quote");

builder->InsertNode(sdtPlainText);
builder->InsertNode(sdtRichText);

ASSERT_EQ(Aspose::Words::NodeType::StructuredDocumentTag, sdtPlainText->get_NodeType());

System::SharedPtr<Aspose::Words::NodeCollection> tags = doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTag, true);

for (auto&& node : System::IterateOver(tags))
{
    auto sdt = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(node);

    std::cout << sdt->get_WordOpenXMLMinimal() << std::endl;

    ASSERT_EQ(Aspose::Words::StyleIdentifier::Quote, sdt->get_Style()->get_StyleIdentifier());
    ASSERT_EQ(u"Quote", sdt->get_StyleName());
}
```

## 另见

* Class [CompositeNode](../../aspose.words/compositenode/)
* Interface [IStructuredDocumentTag](../istructureddocumenttag/)
* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
