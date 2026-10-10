---
title: "Aspose::Words::Section::get_Body method"
linktitle: "get_Body"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Section::get_Body 方法。返回 C++ 中节的 Body 子节点。"
type: docs
weight: 10000
url: /zh/cpp/aspose.words/section/get_body/
---
## Section::get_Body method


返回节的 [Body](../../body/) 子节点。

```cpp
System::SharedPtr<Aspose::Words::Body> Aspose::Words::Section::get_Body()
```

## 备注


[Body](../../body/) contains main text of the section.

如果节的子节点中没有 [Body](../../body/) 节点，则返回 **null**。

## 示例



从文档的所有节中清除主要文本，但保留节本身。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 空白文档包含一个节、一个主体和一个段落。
// 调用 "RemoveAllChildren" 方法以删除所有这些节点，
// 最终得到一个没有子节点的文档节点。
doc->RemoveAllChildren();

// 此文档现在没有可用于添加内容的复合子节点。
// 如果我们想编辑它，需要重新填充其节点集合。
// 首先，创建一个新节，然后将其作为子节点追加到根文档节点。
auto section = System::MakeObject<Aspose::Words::Section>(doc);
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(section);

// 一个节需要一个主体，用于包含并显示其所有内容
// 在页面上位于该节的页眉和页脚之间。
auto body = System::MakeObject<Aspose::Words::Body>(doc);
section->AppendChild<System::SharedPtr<Aspose::Words::Body>>(body);

// 此主体没有子节点，因此我们暂时无法向其添加运行。
ASSERT_EQ(0, doc->get_FirstSection()->get_Body()->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// 调用 "EnsureMinimum" 以确保此主体至少包含一个空段落。
body->EnsureMinimum();

// 现在，我们可以向主体添加运行，并让文档显示它们。
body->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## 另见

* Class [Body](../../body/)
* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
