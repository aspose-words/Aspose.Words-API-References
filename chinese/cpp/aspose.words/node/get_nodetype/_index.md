---
title: "Aspose::Words::Node::get_NodeType 方法"
linktitle: "get_NodeType"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Node::get_NodeType 方法。获取此节点在 C++ 中的类型。"
type: docs
weight: 9000
url: /zh/cpp/aspose.words/node/get_nodetype/
---
## Node::get_NodeType method


获取此节点的类型。

```cpp
virtual Aspose::Words::NodeType Aspose::Words::Node::get_NodeType() const =0
```


## 示例



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


展示如何使用节点的 NextSibling 属性遍历其直接子节点。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");

for (System::SharedPtr<Aspose::Words::Node> node = doc->get_FirstSection()->get_Body()->get_FirstChild(); node != nullptr; node = node->get_NextSibling())
{
    std::cout << std::endl;
    std::cout << System::String::Format(u"Node type: {0}", Aspose::Words::Node::NodeTypeToString(node->get_NodeType())) << std::endl;

    System::String contents = node->GetText().Trim();
    std::cout << (contents == System::String::Empty ? u"This node contains no text" : System::String::Format(u"Contents: \"{0}\"", node->GetText().Trim())) << std::endl;
}
```

## 另见

* Enum [NodeType](../../nodetype/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
