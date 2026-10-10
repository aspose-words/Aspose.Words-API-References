---
title: "Aspose::Words::Markup::StructuredDocumentTagRangeStart 类"
linktitle: "StructuredDocumentTagRangeStart"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Markup::StructuredDocumentTagRangeStart 类。表示接受多节内容的范围结构化文档标签的起始。另请参阅 StructuredDocumentTagRangeEnd。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 14000
url: /zh/cpp/aspose.words.markup/structureddocumenttagrangestart/
---
## StructuredDocumentTagRangeStart class


表示接受多节内容的 **ranged** 结构化文档标签的起始。另请参阅 [StructuredDocumentTagRangeEnd](../structureddocumenttagrangeend/)。欲了解更多，请访问 [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/) 文档文章。

```cpp
class StructuredDocumentTagRangeStart : public Aspose::Words::Node,
                                        public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Node>>,
                                        public Aspose::Words::Markup::IStructuredDocumentTag
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | 接受访问者。 |
| [AppendChild](./appendchild/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 将指定节点添加到 stdContent 范围的末尾。 |
| [Clone](../../aspose.words/node/clone/)(bool) | 创建节点的副本。 |
| [get_Appearance](./get_appearance/)() override | 获取或设置结构化文档标签的外观。 |
| [get_Color](./get_color/)() override | 获取或设置结构化文档标签的颜色。 |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | 指定自定义节点标识符。 |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | 获取此节点所属的文档。 |
| [get_Id](./get_id/)() override | 为此结构化文档标签指定唯一的只读持久数值 Id。 |
| virtual [get_IsComposite](../../aspose.words/node/get_iscomposite/)() | 如果此节点可以包含其他节点，则返回 **true**。 |
| [get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/)() override | 指定此结构化文档标签的内容是否应被解释为包含占位符文本（而非结构化文档标签内的常规文本内容）。如果设置为 **true**，则在打开此文档时恢复此状态（显示占位符文本）。 |
| [get_LastChild](./get_lastchild/)() | 获取 stdContent 范围中的最后一个子项。 |
| [get_Level](./get_level/)() const override | 获取此结构化文档标签范围起始在文档树中的层级。 |
| [get_LockContentControl](./get_lockcontentcontrol/)() override | 设置为 **true** 时，此属性将禁止用户删除此结构化文档标签。 |
| [get_LockContents](./get_lockcontents/)() override | 设置为 **true** 时，此属性将禁止用户编辑此结构化文档标签的内容。 |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | 获取紧随此节点之后的节点。 |
| [get_NodeType](./get_nodetype/)() const override | 返回 [StructuredDocumentTagRangeStart](../../aspose.words/nodetype/)。 |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | 获取此节点的直接父节点。 |
| [get_Placeholder](./get_placeholder/)() override | 获取包含占位符文本的 [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/)，当此结构化文档标签运行内容为空、通过 [XmlMapping](./get_xmlmapping/) 元素指定的关联映射 XML 元素为空，或 [IsShowingPlaceholderText](./get_isshowingplaceholdertext/) 元素为 **true** 时应显示该文本。 |
| [get_PlaceholderName](./get_placeholdername/)() override | 获取或设置包含占位符文本的 [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) 的名称。 |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | 获取紧挨此节点之前的节点。 |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | 返回一个表示包含在此节点中的文档部分的 [Range](../../aspose.words/range/) 对象。 |
| [get_RangeEnd](./get_rangeend/)() | 如果 [StructuredDocumentTag](../structureddocumenttag/) 是范围结构化文档标签，则指定范围的结束。否则返回 **null**。 |
| [get_SdtType](./get_sdttype/)() override | 获取此结构化文档标签的类型。 |
| [get_Tag](./get_tag/)() const override | 指定与当前结构化文档标签节点关联的标签。不能为 **null**。 |
| [get_Title](./get_title/)() const override | 指定与此结构化文档标签关联的友好名称。不能为 **null**。 |
| [get_WordOpenXML](./get_wordopenxml/)() override | 获取一个字符串，表示节点中以 [FlatOpc](../../aspose.words/saveformat/) 格式包含的 XML。 |
| [get_WordOpenXMLMinimal](./get_wordopenxmlminimal/)() | 获取一个字符串，表示以 [FlatOpc](../../aspose.words/saveformat/) 格式包含在节点内的 XML。与 [WordOpenXML](./get_wordopenxml/) 属性不同，此方法生成一个剥离了任何非内容相关部分的精简文档。 |
| [get_XmlMapping](./get_xmlmapping/)() override | 获取一个对象，表示此结构化文档标签范围到当前文档自定义 XML 部分中 XML 数据的映射。 |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | 获取指定 [NodeType](../../aspose.words/nodetype/) 的第一个祖先节点。 |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChildNodes](./getchildnodes/)(Aspose::Words::NodeType, bool) override | 返回一个实时集合，包含匹配指定类型的子节点。 |
| [GetEnumerator](./getenumerator/)() override | 提供对该节点的子节点进行 foreach 样式迭代的支持。 |
| virtual [GetText](../../aspose.words/node/gettext/)() | 获取此节点及其所有子节点的文本。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 根据先序树遍历算法获取下一个节点。 |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | 一个将节点类型枚举值转换为用户友好字符串的实用方法。 |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 根据先序树遍历算法获取上一个节点。 |
| [Remove](../../aspose.words/node/remove/)() | 从父节点中移除自身。 |
| [RemoveAllChildren](./removeallchildren/)() | 移除此范围起始节点和范围结束节点之间的所有节点。 |
| [RemoveSelfOnly](./removeselfonly/)() override | 移除此结构化文档标签的范围起始节点及相应的范围结束节点，但保留其内容在文档树中。 |
| [set_Appearance](./set_appearance/)(Aspose::Words::Markup::SdtAppearance) override | 用于 [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Appearance](./get_appearance/) 的 setter。 |
| [set_Color](./set_color/)(System::Drawing::Color) override | 用于 [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Color](./get_color/) 的 setter。 |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | 用于设置 [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/) 的 setter。 |
| [set_IsShowingPlaceholderText](./set_isshowingplaceholdertext/)(bool) override | 用于 [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/) 的 setter。 |
| [set_LockContentControl](./set_lockcontentcontrol/)(bool) override | 用于 [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_LockContentControl](./get_lockcontentcontrol/) 的 setter。 |
| [set_LockContents](./set_lockcontents/)(bool) override | 用于 [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_LockContents](./get_lockcontents/) 的 setter。 |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PlaceholderName](./set_placeholdername/)(System::String) override | 用于 [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_PlaceholderName](./get_placeholdername/) 的 setter。 |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_Tag](./set_tag/)(System::String) override | 用于 [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Tag](./get_tag/) 的 setter。 |
| [set_Title](./set_title/)(System::String) override | 用于 [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Title](./get_title/) 的 setter。 |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](./settemplateweakptr/)(uint32_t) override |  |
| [StructuredDocumentTagRangeStart](./structureddocumenttagrangestart/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::Markup::SdtType) | 初始化 **Structured document tag range start** 类的新实例。 |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | 以指定格式将节点内容导出为字符串。 |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | 使用指定的保存选项将节点内容导出为字符串。 |
| static [Type](./type/)() |  |

## 示例



展示如何获取多节结构化文档标签的属性。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Multi-section structured document tags.docx");

auto rangeStartTag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeStart>(doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTagRangeStart, true)->idx_get(0));
auto rangeEndTag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeEnd>(doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTagRangeEnd, true)->idx_get(0));

std::cout << "StructuredDocumentTagRangeStart values:" << std::endl;
std::cout << System::String::Format(u"\t|Id: {0}", rangeStartTag->get_Id()) << std::endl;
std::cout << System::String::Format(u"\t|Title: {0}", rangeStartTag->get_Title()) << std::endl;
std::cout << System::String::Format(u"\t|PlaceholderName: {0}", rangeStartTag->get_PlaceholderName()) << std::endl;
std::cout << System::String::Format(u"\t|IsShowingPlaceholderText: {0}", rangeStartTag->get_IsShowingPlaceholderText()) << std::endl;
std::cout << System::String::Format(u"\t|LockContentControl: {0}", rangeStartTag->get_LockContentControl()) << std::endl;
std::cout << System::String::Format(u"\t|LockContents: {0}", rangeStartTag->get_LockContents()) << std::endl;
std::cout << System::String::Format(u"\t|Level: {0}", rangeStartTag->get_Level()) << std::endl;
std::cout << System::String::Format(u"\t|NodeType: {0}", rangeStartTag->get_NodeType()) << std::endl;
std::cout << System::String::Format(u"\t|RangeEnd: {0}", rangeStartTag->get_RangeEnd()) << std::endl;
std::cout << System::String::Format(u"\t|Color: {0}", rangeStartTag->get_Color().ToArgb()) << std::endl;
std::cout << System::String::Format(u"\t|SdtType: {0}", rangeStartTag->get_SdtType()) << std::endl;
std::cout << System::String::Format(u"\t|FlatOpcContent: {0}", rangeStartTag->get_WordOpenXML()) << std::endl;
std::cout << System::String::Format(u"\t|Tag: {0}\n", rangeStartTag->get_Tag()) << std::endl;

std::cout << "StructuredDocumentTagRangeEnd values:" << std::endl;
std::cout << System::String::Format(u"\t|Id: {0}", rangeEndTag->get_Id()) << std::endl;
std::cout << System::String::Format(u"\t|NodeType: {0}", rangeEndTag->get_NodeType()) << std::endl;
```

## 另见

* Class [Node](../../aspose.words/node/)
* Interface [IStructuredDocumentTag](../istructureddocumenttag/)
* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
