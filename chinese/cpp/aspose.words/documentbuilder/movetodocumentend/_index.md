---
title: "Aspose::Words::DocumentBuilder::MoveToDocumentEnd 方法"
linktitle: "MoveToDocumentEnd"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBuilder::MoveToDocumentEnd 方法。将光标移动到文档的末尾（C++）。"
type: docs
weight: 54000
url: /zh/cpp/aspose.words/documentbuilder/movetodocumentend/
---
## DocumentBuilder::MoveToDocumentEnd method


将光标移动到文档末尾。

```cpp
void Aspose::Words::DocumentBuilder::MoveToDocumentEnd()
```


## 示例



展示如何将 DocumentBuilder 的光标移动到文档中的不同节点。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 创建一个有效的书签，这是一个由书签起始节点包围的节点集合，
// 以及书签结束节点。
builder->StartBookmark(u"MyBookmark");
builder->Write(u"Bookmark contents.");
builder->EndBookmark(u"MyBookmark");

System::SharedPtr<Aspose::Words::NodeCollection> firstParagraphNodes = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetChildNodes(Aspose::Words::NodeType::Any, false);

ASSERT_EQ(Aspose::Words::NodeType::BookmarkStart, firstParagraphNodes->idx_get(0)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Run, firstParagraphNodes->idx_get(1)->get_NodeType());
ASSERT_EQ(u"Bookmark contents.", firstParagraphNodes->idx_get(1)->GetText().Trim());
ASSERT_EQ(Aspose::Words::NodeType::BookmarkEnd, firstParagraphNodes->idx_get(2)->get_NodeType());

// DocumentBuilder 的光标始终位于我们上次使用它添加的节点之前。
// 如果构建器的光标位于文档末尾，则其当前节点将为 null。
// 上一个节点是我们上次添加的书签结束节点。
// 使用构建器添加新节点将把它们附加到最后一个节点。
ASSERT_TRUE(System::TestTools::IsNull(builder->get_CurrentNode()));

// 如果我们希望使用构建器编辑文档的其他部分，
// 我们需要将其光标移动到我们想要编辑的节点。
builder->MoveToBookmark(u"MyBookmark");

// 将其移动到书签会将光标定位到书签起始和结束节点之间的第一个节点，即包含的 run。
ASPOSE_ASSERT_EQ(firstParagraphNodes->idx_get(1), builder->get_CurrentNode());

// 我们也可以像这样将光标移动到单个节点。
builder->MoveTo(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetChildNodes(Aspose::Words::NodeType::Any, false)->idx_get(0));

ASSERT_EQ(Aspose::Words::NodeType::BookmarkStart, builder->get_CurrentNode()->get_NodeType());
ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body()->get_FirstParagraph(), builder->get_CurrentParagraph());
ASSERT_TRUE(builder->get_IsAtStartOfParagraph());

// 我们可以使用特定的方法将光标移动到文档的开始/结束位置。
builder->MoveToDocumentEnd();

ASSERT_TRUE(builder->get_IsAtEndOfParagraph());

builder->MoveToDocumentStart();

ASSERT_TRUE(builder->get_IsAtStartOfParagraph());
```

## 另见

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
