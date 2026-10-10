---
title: "Aspose::Words::Document::StartTrackRevisions 方法"
linktitle: "StartTrackRevisions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::StartTrackRevisions 方法。开始自动将您对文档所做的后续程序化更改标记为修订更改（在 C++ 中）。"
type: docs
weight: 92000
url: /zh/cpp/aspose.words/document/starttrackrevisions/
---
## Document::StartTrackRevisions(const System::String\&) method


自动开始将您对文档所做的所有后续更改标记为修订更改。

```cpp
void Aspose::Words::Document::StartTrackRevisions(const System::String &author)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 作者 | const System::String\& | 用于修订的作者缩写。 |
## 备注


如果您调用此方法后以编程方式对文档进行一些更改，保存文档，然后在 MS Word 中打开文档，您将看到这些更改被标记为修订。

目前 Aspose.Words 仅支持对节点插入和删除的跟踪。格式更改不会记录为修订。

在通过节点操作修改此文档以及使用 [DocumentBuilder](../../documentbuilder/) 时，都支持自动更改跟踪。

此方法不会更改 [TrackRevisions](../get_trackrevisions/) 选项，也不会在修订跟踪中使用其值。

## 示例



展示如何在编辑文档时跟踪修订。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 编辑文档通常不会算作修订，除非我们开始跟踪它们。
builder->Write(u"Hello world! ");

ASSERT_EQ(0, doc->get_Revisions()->get_Count());
ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(0)->get_IsInsertRevision());

doc->StartTrackRevisions(u"John Doe");

builder->Write(u"Hello again! ");

ASSERT_EQ(1, doc->get_Revisions()->get_Count());
ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(1)->get_IsInsertRevision());
ASSERT_EQ(u"John Doe", doc->get_Revisions()->idx_get(0)->get_Author());
ASSERT_TRUE((System::DateTime::get_Now() - doc->get_Revisions()->idx_get(0)->get_DateTime()).get_Milliseconds() <= 10);

// 停止跟踪修订，以免将任何后续编辑计为修订。
doc->StopTrackRevisions();
builder->Write(u"Hello again! ");

ASSERT_EQ(1, doc->get_Revisions()->get_Count());
ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(2)->get_IsInsertRevision());

// 创建修订会为其分配操作的日期和时间。
// 当我们开始跟踪修订时，可以通过传递 DateTime.MinValue 来禁用此功能。
doc->StartTrackRevisions(u"John Doe", System::DateTime::MinValue);
builder->Write(u"Hello again! ");

ASSERT_EQ(2, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"John Doe", doc->get_Revisions()->idx_get(1)->get_Author());
ASSERT_EQ(System::DateTime::MinValue, doc->get_Revisions()->idx_get(1)->get_DateTime());

// 我们可以通过编程方式接受/拒绝这些修订
// 例如调用 Document.AcceptAllRevisions 方法，或每个修订的 Accept 方法。
// 在 Microsoft Word 中，我们可以通过 “审阅” → “更改” 手动处理它们。
doc->Save(get_ArtifactsDir() + u"Revision.StartTrackRevisions.docx");
```

## 另见

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::StartTrackRevisions(const System::String\&, System::DateTime) method


自动开始将您对文档所做的所有后续更改标记为修订更改。

```cpp
void Aspose::Words::Document::StartTrackRevisions(const System::String &author, System::DateTime dateTime)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 作者 | const System::String\& | 用于修订的作者缩写。 |
| dateTime | System::DateTime | 用于修订的日期和时间。 |
## 备注


如果您调用此方法后以编程方式对文档进行一些更改，保存文档，然后在 MS Word 中打开文档，您将看到这些更改被标记为修订。

目前 Aspose.Words 仅支持对节点插入和删除的跟踪。格式更改不会记录为修订。

在通过节点操作修改此文档以及使用 [DocumentBuilder](../../documentbuilder/) 时，都支持自动更改跟踪。

此方法不会更改 [TrackRevisions](../get_trackrevisions/) 选项，也不会在修订跟踪中使用其值。

## 示例



展示如何在编辑文档时跟踪修订。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 编辑文档通常不会算作修订，除非我们开始跟踪它们。
builder->Write(u"Hello world! ");

ASSERT_EQ(0, doc->get_Revisions()->get_Count());
ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(0)->get_IsInsertRevision());

doc->StartTrackRevisions(u"John Doe");

builder->Write(u"Hello again! ");

ASSERT_EQ(1, doc->get_Revisions()->get_Count());
ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(1)->get_IsInsertRevision());
ASSERT_EQ(u"John Doe", doc->get_Revisions()->idx_get(0)->get_Author());
ASSERT_TRUE((System::DateTime::get_Now() - doc->get_Revisions()->idx_get(0)->get_DateTime()).get_Milliseconds() <= 10);

// 停止跟踪修订，以免将任何后续编辑计为修订。
doc->StopTrackRevisions();
builder->Write(u"Hello again! ");

ASSERT_EQ(1, doc->get_Revisions()->get_Count());
ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(2)->get_IsInsertRevision());

// 创建修订会为其分配操作的日期和时间。
// 当我们开始跟踪修订时，可以通过传递 DateTime.MinValue 来禁用此功能。
doc->StartTrackRevisions(u"John Doe", System::DateTime::MinValue);
builder->Write(u"Hello again! ");

ASSERT_EQ(2, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"John Doe", doc->get_Revisions()->idx_get(1)->get_Author());
ASSERT_EQ(System::DateTime::MinValue, doc->get_Revisions()->idx_get(1)->get_DateTime());

// 我们可以通过编程方式接受/拒绝这些修订
// 例如调用 Document.AcceptAllRevisions 方法，或每个修订的 Accept 方法。
// 在 Microsoft Word 中，我们可以通过 “审阅” → “更改” 手动处理它们。
doc->Save(get_ArtifactsDir() + u"Revision.StartTrackRevisions.docx");
```

## 另见

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
