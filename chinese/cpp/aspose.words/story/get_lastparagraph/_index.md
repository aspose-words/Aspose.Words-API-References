---
title: "Aspose::Words::Story::get_LastParagraph 方法"
linktitle: "get_LastParagraph"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Story::get_LastParagraph 方法。获取 C++ 中故事的最后一个段落。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words/story/get_lastparagraph/
---
## Story::get_LastParagraph method


获取故事中的最后一个段落。

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::Story::get_LastParagraph() override
```


## 示例



展示如何将 [DocumentBuilder](../../documentbuilder/) 的光标位置移动到指定节点。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Run 1. ");

// 文档构建器有一个光标，它充当文档的一部分
// 在我们使用其文档构建方法时，构建器会在此处追加新节点。
// 此光标的功能与 Microsoft Word 的闪烁光标相同，
// 并且它总是紧随构建器刚插入的任何节点之后。
// 要将内容追加到文档的其他部分，
// 我们可以使用 "MoveTo" 方法将光标移动到不同的节点。
builder->MoveTo(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0));

// 光标现在位于我们移动到的节点前面。
// 添加第二个运行将把它插入到第一个运行之前。
builder->Writeln(u"Run 2. ");

ASSERT_EQ(u"Run 2. \rRun 1.", doc->GetText().Trim());

// 将光标移动到文档末尾，以继续像之前一样在末尾追加文本。
builder->MoveTo(doc->get_LastSection()->get_Body()->get_LastParagraph());
builder->Writeln(u"Run 3. ");

ASSERT_EQ(u"Run 2. \rRun 1. \rRun 3.", doc->GetText().Trim());
```

## 另见

* Class [Paragraph](../../paragraph/)
* Class [Story](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
