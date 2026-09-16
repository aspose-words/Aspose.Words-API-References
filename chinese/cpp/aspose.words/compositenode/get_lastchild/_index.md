---
title: "Aspose::Words::CompositeNode::get_LastChild 方法"
linktitle: "get_LastChild"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::CompositeNode::get_LastChild 方法。获取节点的最后一个子节点（C++）。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words/compositenode/get_lastchild/
---
## CompositeNode::get_LastChild method


获取节点的最后一个子节点。

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::CompositeNode::get_LastChild() const
```


## 示例



展示如何使用 [Node](../../node/) 和 [CompositeNode](../) 的方法在文档中删除倒数第二个节之前的节。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Section 1 text.");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakContinuous);
builder->Writeln(u"Section 2 text.");

// 这两个节彼此是兄弟节点。
auto lastSection = System::ExplicitCast<Aspose::Words::Section>(doc->get_LastChild());
auto firstSection = System::ExplicitCast<Aspose::Words::Section>(lastSection->get_PreviousSibling());

// 根据节与另一节的兄弟关系删除该节。
if (lastSection->get_PreviousSibling() != nullptr)
{
    doc->RemoveChild<System::SharedPtr<Aspose::Words::Section>>(firstSection);
}

// 我们删除的节是第一节，文档只剩下第二节。
ASSERT_EQ(u"Section 2 text.", doc->GetText().Trim());
```

## 另见

* Class [Node](../../node/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
