---
title: "Aspose::Words::DocumentBuilder::MoveToBookmark 方法"
linktitle: "MoveToBookmark"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBuilder::MoveToBookmark 方法。将光标移动到书签（C++）。"
type: docs
weight: 52000
url: /zh/cpp/aspose.words/documentbuilder/movetobookmark/
---
## DocumentBuilder::MoveToBookmark(const System::String\&) method


将光标移动到书签。

```cpp
bool Aspose::Words::DocumentBuilder::MoveToBookmark(const System::String &bookmarkName)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| bookmarkName | const System::String\& | 要将光标移动到的书签名称。 |

### ReturnValue

**true** if the bookmark was found; **false** otherwise.
## 备注


将光标移动到指定名称的书签起始位置之后的一个位置。

比较不区分大小写。如果未找到书签，则返回 **false**，且光标不移动。

插入新文本不会替换书签中已有的文本。

请注意，文档中的某些书签被分配给表单字段。移动到此类书签并在那里插入文本会将文本插入表单字段代码中。虽然这不会使表单字段失效，但插入的文本不会可见，因为它成为字段代码的一部分。

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
## DocumentBuilder::MoveToBookmark(const System::String\&, bool, bool) method


将光标更精确地移动到书签。

```cpp
bool Aspose::Words::DocumentBuilder::MoveToBookmark(const System::String &bookmarkName, bool isStart, bool isAfter)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| bookmarkName | const System::String\& | 要将光标移动到的书签名称。 |
| isStart | bool | 当 **true** 时，将光标移动到书签的开始位置。当 **false** 时，将光标移动到书签的结束位置。 |
| isAfter | bool | 当 **true** 时，将光标移动到书签起始或结束位置之后。当 **false** 时，将光标移动到书签起始或结束位置之前。 |

### ReturnValue

**true** if the bookmark was found; **false** otherwise.
## 备注


将光标移动到书签起始或结束位置之前或之后的一个位置。

如果期望的位置不是行内级别，则移动到下一个段落。

比较不区分大小写。如果未找到书签，则返回 **false**，且光标不移动。

## 示例



展示如何将 DocumentBuilder 的节点插入点光标移动到书签。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 有效的书签由一个 BookmarkStart 节点、一个带有
// 匹配的书签名称（位于后方），以及被这些节点包围的内容组成。
builder->StartBookmark(u"MyBookmark");
builder->Write(u"Hello world! ");
builder->EndBookmark(u"MyBookmark");

// 将 DocumentBuilder 的光标移动到书签有 4 种方式。
// 如果我们位于 BookmarkStart 和 BookmarkEnd 节点之间，光标将位于书签内部。
// 这意味着构建器添加的任何文本都将成为书签的一部分。
// 1 -  书签外部，在 BookmarkStart 节点之前：
ASSERT_TRUE(builder->MoveToBookmark(u"MyBookmark", true, false));
builder->Write(u"1. ");

ASSERT_EQ(u"Hello world! ", doc->get_Range()->get_Bookmarks()->idx_get(u"MyBookmark")->get_Text());
ASSERT_EQ(u"1. Hello world!", doc->GetText().Trim());

// 2 -  书签内部，紧跟在 BookmarkStart 节点之后：
ASSERT_TRUE(builder->MoveToBookmark(u"MyBookmark", true, true));
builder->Write(u"2. ");

ASSERT_EQ(u"2. Hello world! ", doc->get_Range()->get_Bookmarks()->idx_get(u"MyBookmark")->get_Text());
ASSERT_EQ(u"1. 2. Hello world!", doc->GetText().Trim());

// 2 -  书签内部，正好在 BookmarkEnd 节点之前：
ASSERT_TRUE(builder->MoveToBookmark(u"MyBookmark", false, false));
builder->Write(u"3. ");

ASSERT_EQ(u"2. Hello world! 3. ", doc->get_Range()->get_Bookmarks()->idx_get(u"MyBookmark")->get_Text());
ASSERT_EQ(u"1. 2. Hello world! 3.", doc->GetText().Trim());

// 4 -  书签外部，在 BookmarkEnd 节点之后：
ASSERT_TRUE(builder->MoveToBookmark(u"MyBookmark", false, true));
builder->Write(u"4.");

ASSERT_EQ(u"2. Hello world! 3. ", doc->get_Range()->get_Bookmarks()->idx_get(u"MyBookmark")->get_Text());
ASSERT_EQ(u"1. 2. Hello world! 3. 4.", doc->GetText().Trim());
```

## 另见

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
