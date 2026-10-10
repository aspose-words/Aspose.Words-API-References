---
title: "Aspose::Words::CompositeNode::GetChild 方法"
linktitle: "GetChild"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::CompositeNode::GetChild 方法。返回在 C++ 中匹配指定类型的第 N 个子节点。"
type: docs
weight: 9000
url: /zh/cpp/aspose.words/compositenode/getchild/
---
## CompositeNode::GetChild method


返回匹配指定类型的第 N 个子节点。

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::CompositeNode::GetChild(Aspose::Words::NodeType nodeType, int32_t index, bool isDeep)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| nodeType | Aspose::Words::NodeType | 指定子节点的类型。 |
| index | int32_t | 要选择的子节点的零基索引。也允许使用负索引，表示从末尾访问，例如 -1 表示最后一个节点。 |
| isDeep | bool | **true** 表示递归地从所有子节点中选择；**false** 表示仅在直接子节点中选择。更多信息请参见备注。 |

### ReturnValue

匹配条件的子节点，如果未找到匹配的节点则为 **null**。
## 备注


如果索引超出范围，将返回 **null**。

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

* Class [Node](../../node/)
* Enum [NodeType](../../nodetype/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
