---
title: "Aspose::Words::Node::NextPreOrder method"
linktitle: "NextPreOrder"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Node::NextPreOrder method. 根据 C++ 中的先序树遍历算法获取下一个节点。"
type: docs
weight: 18000
url: /zh/cpp/aspose.words/node/nextpreorder/
---
## Node::NextPreOrder method


根据先序树遍历算法获取下一个节点。

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::Node::NextPreOrder(const System::SharedPtr<Aspose::Words::Node> &rootNode)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| rootNode | const System::SharedPtr\<Aspose::Words::Node\>\& | 遍历的顶层节点（限制）。 |

### ReturnValue

先序顺序中的下一个节点。如果达到 *rootNode*，则为 Null。

## 示例



展示如何使用先序遍历算法遍历文档的节点树，并删除遇到的任何带图像的形状。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

ASSERT_EQ(9, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Shape>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Shape> s)>>([](System::SharedPtr<Aspose::Words::Drawing::Shape> s) -> bool
{
    return s->get_HasImage();
}))));

System::SharedPtr<Aspose::Words::Node> curNode = doc;
while (curNode != nullptr)
{
    System::SharedPtr<Aspose::Words::Node> nextNode = curNode->NextPreOrder(doc);

    if (curNode->PreviousPreOrder(doc) != nullptr && nextNode != nullptr)
    {
        ASPOSE_ASSERT_EQ(curNode, nextNode->PreviousPreOrder(doc));
    }

    if (curNode->get_NodeType() == Aspose::Words::NodeType::Shape && (System::ExplicitCast<Aspose::Words::Drawing::Shape>(curNode))->get_HasImage())
    {
        curNode->Remove();
    }

    curNode = nextNode;
}

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Shape>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Shape> s)>>([](System::SharedPtr<Aspose::Words::Drawing::Shape> s) -> bool
{
    return s->get_HasImage();
}))));
```

## 另见

* Class [Node](../)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
