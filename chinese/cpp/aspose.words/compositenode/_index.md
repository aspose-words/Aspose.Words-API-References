---
title: "Aspose::Words::CompositeNode 类"
linktitle: "CompositeNode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::CompositeNode 类。用于可以包含其他节点的节点的基类。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 15000
url: /zh/cpp/aspose.words/compositenode/
---
## CompositeNode class


可包含其他节点的节点的基类。要了解更多信息，请访问 [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/) 文档文章。

```cpp
class CompositeNode : public Aspose::Words::Node,
                      public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Node>>,
                      public Aspose::Words::INodeCollection
```

## 方法

| 方法 | 描述 |
| --- | --- |
| virtual [Accept](../node/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | 接受访问者。 |
| virtual [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | 当在派生类中实现时，调用指定文档访问器的 VisitXXXEnd 方法。 |
| virtual [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | 当在派生类中实现时，调用指定文档访问器的 VisitXXXStart 方法。 |
| [AppendChild](./appendchild/)(T) |  |
| [Clone](../node/clone/)(bool) | 创建节点的副本。 |
| [get_Count](./get_count/)() | 获取此节点的直接子节点数量。 |
| [get_CustomNodeId](../node/get_customnodeid/)() const | 指定自定义节点标识符。 |
| virtual [get_Document](../node/get_document/)() const | 获取此节点所属的文档。 |
| [get_FirstChild](./get_firstchild/)() const | 获取节点的第一个子节点。 |
| [get_HasChildNodes](./get_haschildnodes/)() | 如果此节点有任何子节点，则返回 **true**。 |
| [get_IsComposite](./get_iscomposite/)() override | 因为此节点可以拥有子节点，返回 **true**。 |
| [get_LastChild](./get_lastchild/)() const | 获取节点的最后一个子节点。 |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | 获取紧随此节点之后的节点。 |
| virtual [get_NodeType](../node/get_nodetype/)() const | 获取此节点的类型。 |
| [get_ParentNode](../node/get_parentnode/)() | 获取此节点的直接父节点。 |
| [get_PreviousSibling](../node/get_previoussibling/)() | 获取紧挨此节点之前的节点。 |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | 返回一个 [Range](../range/) 对象，表示此节点中包含的文档部分。 |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | 获取指定 [NodeType](../nodetype/) 的第一个祖先。 |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetChild](./getchild/)(Aspose::Words::NodeType, int32_t, bool) | 返回匹配指定类型的第 N 个子节点。 |
| [GetChildNodes](./getchildnodes/)(Aspose::Words::NodeType, bool) | 返回匹配指定类型的子节点的实时集合。 |
| [GetEnumerator](./getenumerator/)() override | 提供对该节点的子节点进行 foreach 样式迭代的支持。 |
| [GetText](./gettext/)() override | 获取此节点及其所有子节点的文本。 |
| [GetType](./gettype/)() const override |  |
| [IndexOf](./indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 返回指定子节点在子节点数组中的索引。 |
| [InsertAfter](./insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](./insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 根据先序树遍历算法获取下一个节点。 |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | 一个将节点类型枚举值转换为用户友好字符串的实用方法。 |
| [PrependChild](./prependchild/)(T) |  |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 根据先序树遍历算法获取上一个节点。 |
| [Remove](../node/remove/)() | 从父节点中移除自身。 |
| [RemoveAllChildren](./removeallchildren/)() | 移除当前节点的所有子节点。 |
| [RemoveChild](./removechild/)(T) |  |
| [RemoveSmartTags](./removesmarttags/)() | 移除当前节点的所有 [SmartTag](../../aspose.words.markup/smarttag/) 后代节点。 |
| [SelectNodes](./selectnodes/)(const System::String\&) | 选择匹配 XPath 表达式的节点列表。 |
| [SelectSingleNode](./selectsinglenode/)(const System::String\&) | 选择匹配 XPath 表达式的第一个 [Node](../node/)。 |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | 设置 [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/) 的值。 |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](./settemplateweakptr/)(uint32_t) override |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | 以指定格式将节点内容导出为字符串。 |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | 使用指定的保存选项将节点内容导出为字符串。 |
| static [Type](./type/)() |  |
## 备注


文档表示为节点树，类似于 DOM 或 XmlDocument。

欲了解更多信息，请参阅组合设计模式。

该 [CompositeNode](./) 类：

* Provides access to the child nodes.
* Implements Composite operations such as insert and remove children.
* Provides methods for XPath navigation.



## 示例



展示如何遍历复合节点的子节点集合。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 向本文档的第一段添加两个运行和一个形状作为子节点。
auto paragraph = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world! "));

auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(200);
shape->set_Height(200);
// 请注意，'CustomNodeId' 不会保存到输出文件中，仅在节点生命周期内存在。
shape->set_CustomNodeId(100);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello again!"));

// 遍历段落的直接子节点集合，
// 并打印我们在其中找到的任何运行或形状。
System::SharedPtr<Aspose::Words::NodeCollection> children = paragraph->GetChildNodes(Aspose::Words::NodeType::Any, false);

ASSERT_EQ(3, paragraph->GetChildNodes(Aspose::Words::NodeType::Any, false)->get_Count());

for (auto&& child : System::IterateOver(children))
{
    switch (child->get_NodeType())
    {
        case Aspose::Words::NodeType::Run:
            std::cout << "Run contents:" << std::endl;
            std::cout << System::String::Format(u"\t\"{0}\"", child->GetText().Trim()) << std::endl;
            break;

        case Aspose::Words::NodeType::Shape:
        {
            auto childShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(child);
            std::cout << "Shape:" << std::endl;
            std::cout << System::String::Format(u"\t{0}, {1}x{2}", childShape->get_ShapeType(), childShape->get_Width(), childShape->get_Height()) << std::endl;
            ASSERT_EQ(100, shape->get_CustomNodeId());
            break;
        }

        default:
            break;
    }
}
```

## 另见

* Class [Node](../node/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
