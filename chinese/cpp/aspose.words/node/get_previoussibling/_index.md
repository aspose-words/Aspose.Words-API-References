---
title: "Aspose::Words::Node::get_PreviousSibling method"
linktitle: "get_PreviousSibling"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Node::get_PreviousSibling method. 在 C++ 中获取紧邻此节点之前的节点。"
type: docs
weight: 11000
url: /zh/cpp/aspose.words/node/get_previoussibling/
---
## Node::get_PreviousSibling method


获取紧挨此节点之前的节点。

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::Node::get_PreviousSibling()
```


## 示例



展示如何使用 [Node](../) 和 [CompositeNode](../../compositenode/) 的方法来删除文档中倒数第二节之前的节。
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

* Class [Node](../)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
