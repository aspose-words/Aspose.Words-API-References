---
title: "Aspose::Words::Node 类"
linktitle: "Node"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Node 类。Word 文档中所有节点的基类。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 41000
url: /zh/cpp/aspose.words/node/
---
## Node class


Word 文档中所有节点的基类。要了解更多，请访问 [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/) 文档文章。

```cpp
class Node : public virtual System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| virtual [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | 接受访问者。 |
| [Clone](./clone/)(bool) | 创建节点的副本。 |
| [get_CustomNodeId](./get_customnodeid/)() const | 指定自定义节点标识符。 |
| virtual [get_Document](./get_document/)() const | 获取此节点所属的文档。 |
| virtual [get_IsComposite](./get_iscomposite/)() | 如果此节点可以包含其他节点，则返回 **true**。 |
| [get_NextNode](./get_nextnode/)() const |  |
| [get_NextSibling](./get_nextsibling/)() | 获取紧随此节点之后的节点。 |
| virtual [get_NodeType](./get_nodetype/)() const | 获取此节点的类型。 |
| [get_ParentNode](./get_parentnode/)() | 获取此节点的直接父节点。 |
| [get_PreviousSibling](./get_previoussibling/)() | 获取紧挨此节点之前的节点。 |
| [get_PrevNode](./get_prevnode/)() const |  |
| [get_Range](./get_range/)() | 返回一个 [Range](../range/) 对象，表示此节点中包含的文档部分。 |
| [GetAncestor](./getancestor/)(Aspose::Words::NodeType) | 获取指定 [NodeType](../nodetype/) 的第一个祖先。 |
| [GetAncestorOf](./getancestorof/)() |  |
| virtual [GetText](./gettext/)() | 获取此节点及其所有子节点的文本。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](./isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](./nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 根据先序树遍历算法获取下一个节点。 |
| static [NodeTypeToString](./nodetypetostring/)(Aspose::Words::NodeType) | 一个将节点类型枚举值转换为用户友好字符串的实用方法。 |
| [PreviousPreOrder](./previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 根据先序树遍历算法获取上一个节点。 |
| [Remove](./remove/)() | 从父节点中移除自身。 |
| [set_CustomNodeId](./set_customnodeid/)(int32_t) | 用于 [Aspose::Words::Node::get_CustomNodeId](./get_customnodeid/) 的设置器。 |
| [set_NextNode](./set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](./set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](./setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [ToString](./tostring/)(Aspose::Words::SaveFormat) | 以指定格式将节点内容导出为字符串。 |
| [ToString](./tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | 使用指定的保存选项将节点内容导出为字符串。 |
| static [Type](./type/)() |  |
## 备注


文档表示为节点树，类似于 DOM 或 XmlDocument。

欲了解更多信息，请参阅组合设计模式。

该 [Node](./) 类：

* Defines the child node interface.
* Defines the interface for visiting nodes.
* Provides default cloning capability.
* Implements parent node and owner document mechanisms.
* Implements access to sibling nodes.



## 示例



展示如何克隆复合节点。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

// 下面有两种克隆复合节点的方法。
// 1 -  创建节点的克隆，并同时创建其每个子节点的克隆。
System::SharedPtr<Aspose::Words::Node> cloneWithChildren = System::ExplicitCast<Aspose::Words::Node>(para)->Clone(true);

ASSERT_TRUE((System::ExplicitCast<Aspose::Words::CompositeNode>(cloneWithChildren))->get_HasChildNodes());
ASSERT_EQ(u"Hello world!", cloneWithChildren->GetText().Trim());

// 2 -  仅创建节点本身的克隆，不包含任何子节点。
System::SharedPtr<Aspose::Words::Node> cloneWithoutChildren = System::ExplicitCast<Aspose::Words::Node>(para)->Clone(false);

ASSERT_FALSE((System::ExplicitCast<Aspose::Words::CompositeNode>(cloneWithoutChildren))->get_HasChildNodes());
ASSERT_EQ(System::String::Empty, cloneWithoutChildren->GetText().Trim());
```


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


展示如何从复合节点中移除特定类型的所有子节点。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

ASSERT_EQ(2, doc->GetChildNodes(Aspose::Words::NodeType::Table, true)->get_Count());

System::SharedPtr<Aspose::Words::Node> curNode = doc->get_FirstSection()->get_Body()->get_FirstChild();

while (curNode != nullptr)
{
    // 将下一个兄弟节点保存为变量，以防在删除此节点后想要移动到它。
    System::SharedPtr<Aspose::Words::Node> nextNode = curNode->get_NextSibling();

    // 节主体可以包含 Paragraph 和 Table 节点。
    // 如果节点是 Table，则将其从父节点中移除。
    if (curNode->get_NodeType() == Aspose::Words::NodeType::Table)
    {
        curNode->Remove();
    }

    curNode = nextNode;
}

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Table, true)->get_Count());
```

## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
