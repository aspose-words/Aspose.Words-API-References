---
title: "Aspose::Words::Node::Clone 方法"
linktitle: "克隆"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Node::Clone 方法。创建该节点在 C++ 中的副本。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words/node/clone/
---
## Node::Clone method


创建节点的副本。

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::Node::Clone(bool isCloneChildren)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| isCloneChildren | bool | 设为 True 时递归克隆指定节点下的子树；设为 false 时仅克隆节点本身。 |

### ReturnValue

克隆的节点。
## 备注


此方法充当节点的复制构造函数。克隆的节点没有父节点，但属于与原始节点相同的文档。

此方法始终对节点执行深拷贝。*isCloneChildren* 参数指定是否同时复制所有子节点。

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

## 另见

* Class [Node](../)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
