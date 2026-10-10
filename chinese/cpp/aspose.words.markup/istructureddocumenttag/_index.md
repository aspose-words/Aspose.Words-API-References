---
title: "Aspose::Words::Markup::IStructuredDocumentTag 接口"
linktitle: "IStructuredDocumentTag"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Markup::IStructuredDocumentTag 接口。用于在 C++ 中为 StructuredDocumentTag 和 StructuredDocumentTagRangeStart 定义通用数据的接口。"
type: docs
weight: 16000
url: /zh/cpp/aspose.words.markup/istructureddocumenttag/
---
## IStructuredDocumentTag interface


用于为 [StructuredDocumentTag](../structureddocumenttag/) 和 [StructuredDocumentTagRangeStart](../structureddocumenttagrangestart/) 定义通用数据的接口。

```cpp
class IStructuredDocumentTag : public virtual System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| virtual [get_Appearance](./get_appearance/)() | 获取或设置结构化文档标签的外观。 |
| virtual [get_Color](./get_color/)() | 获取或设置结构化文档标签的颜色。 |
| virtual [get_Id](./get_id/)() | 为此 **SDT** 指定唯一的只读持久数值 Id。 |
| virtual [get_IsMultiSection](./get_ismultisection/)() | 如果此实例是范围（多节）结构化文档标签，则返回 true。 |
| virtual [get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/)() | 指定此 **SDT** 的内容是否应被解释为包含占位符文本（而不是 **SDT** 内的常规文本内容）。如果设置为 true，则在打开文档时将恢复此状态（显示占位符文本）。 |
| virtual [get_Level](./get_level/)() const | 获取此 **SDT** 在文档树中出现的层级。 |
| virtual [get_LockContentControl](./get_lockcontentcontrol/)() | 设置为 true 时，此属性将阻止用户删除此 **SDT**。 |
| virtual [get_LockContents](./get_lockcontents/)() | 设置为 true 时，此属性将阻止用户编辑此 **SDT** 的内容。 |
| virtual [get_Node](./get_node/)() | 返回实现此接口的 [Node](../../aspose.words/node/) 对象。 |
| virtual [get_Placeholder](./get_placeholder/)() | 获取包含占位符文本的 [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/)，当此 SDT 运行内容为空、通过 [XmlMapping](./get_xmlmapping/) 元素指定的关联映射 XML 元素为空，或 [IsShowingPlaceholderText](./get_isshowingplaceholdertext/) 元素为 true 时，应显示该占位符文本。 |
| virtual [get_PlaceholderName](./get_placeholdername/)() | 获取或设置包含占位符文本的 [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) 的名称。 |
| virtual [get_SdtType](./get_sdttype/)() | 获取此 **Structured document tag** 的类型。 |
| virtual [get_Tag](./get_tag/)() const | 指定与当前 SDT 节点关联的标签。不能为空。 |
| virtual [get_Title](./get_title/)() const | 指定与此 **SDT** 关联的友好名称。不能为空。 |
| virtual [get_WordOpenXML](./get_wordopenxml/)() | 获取一个字符串，表示节点中以 [FlatOpc](../../aspose.words/saveformat/) 格式包含的 XML。 |
| virtual [get_XmlMapping](./get_xmlmapping/)() | 获取一个对象，表示此结构化文档标签映射到当前文档的自定义 XML 部分中的 XML 数据。 |
| virtual [GetChildNodes](./getchildnodes/)(Aspose::Words::NodeType, bool) | 返回一个实时集合，包含匹配指定类型的子节点。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [RemoveSelfOnly](./removeselfonly/)() | 仅删除此 SDT 节点本身，但保留其内容在文档树中。 |
| virtual [set_Appearance](./set_appearance/)(Aspose::Words::Markup::SdtAppearance) | 用于设置 [Aspose::Words::Markup::IStructuredDocumentTag::get_Appearance](./get_appearance/) 的 setter。 |
| virtual [set_Color](./set_color/)(System::Drawing::Color) | 用于设置 [Aspose::Words::Markup::IStructuredDocumentTag::get_Color](./get_color/) 的 setter。 |
| virtual [set_IsShowingPlaceholderText](./set_isshowingplaceholdertext/)(bool) | 用于设置 [Aspose::Words::Markup::IStructuredDocumentTag::get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/) 的 setter。 |
| virtual [set_LockContentControl](./set_lockcontentcontrol/)(bool) | 用于设置 [Aspose::Words::Markup::IStructuredDocumentTag::get_LockContentControl](./get_lockcontentcontrol/) 的 setter。 |
| virtual [set_LockContents](./set_lockcontents/)(bool) | 用于设置 [Aspose::Words::Markup::IStructuredDocumentTag::get_LockContents](./get_lockcontents/) 的 setter。 |
| virtual [set_PlaceholderName](./set_placeholdername/)(System::String) | 用于设置 [Aspose::Words::Markup::IStructuredDocumentTag::get_PlaceholderName](./get_placeholdername/) 的 setter。 |
| virtual [set_Tag](./set_tag/)(System::String) | 用于设置 [Aspose::Words::Markup::IStructuredDocumentTag::get_Tag](./get_tag/) 的 setter。 |
| virtual [set_Title](./set_title/)(System::String) | 用于设置 [Aspose::Words::Markup::IStructuredDocumentTag::get_Title](./get_title/) 的 setter。 |
| static [Type](./type/)() |  |

## 示例



展示如何删除结构化文档标签，但保留内部内容。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

// 此集合提供统一接口，用于访问有范围和无范围的结构化标签。
System::SharedPtr<System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag>>> sdts = doc->get_Range()->get_StructuredDocumentTags()->LINQ_ToList();
ASSERT_EQ(5, sdts->LINQ_Count());

// 在此我们可以通过有范围和无范围结构化标签的通用接口获取子节点。
for (auto&& sdt : System::IterateOver(sdts))
{
    if (sdt->GetChildNodes(Aspose::Words::NodeType::Any, false)->get_Count() > 0)
    {
        sdt->RemoveSelfOnly();
    }
}

sdts = doc->get_Range()->get_StructuredDocumentTags()->LINQ_ToList();
ASSERT_EQ(0, sdts->LINQ_Count());
```

## 另见

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
