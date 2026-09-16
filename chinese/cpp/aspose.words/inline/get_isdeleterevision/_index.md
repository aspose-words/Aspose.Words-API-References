---
title: "Aspose::Words::Inline::get_IsDeleteRevision 方法"
linktitle: "get_IsDeleteRevision"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Inline::get_IsDeleteRevision 方法。返回 true，如果此对象在 Microsoft Word 中启用了更改跟踪时被删除（使用 C++）。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words/inline/get_isdeleterevision/
---
## Inline::get_IsDeleteRevision method


如果在启用更改跟踪的 Microsoft Word 中删除了此对象，则返回 true。

```cpp
bool Aspose::Words::Inline::get_IsDeleteRevision()
```


## 示例



展示如何确定内联节点的修订类型。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revision runs.docx");

// 当我们在文档中编辑时，如果通过 “审阅 -> 跟踪更改” 找到的 \"Track Changes\" 选项已开启，
// 在 Microsoft Word 中已打开时，我们所做的更改将计为修订。
// 使用 Aspose.Words 编辑文档时，我们可以通过以下方式开始跟踪修订：
// 调用文档的 \"StartTrackRevisions\" 方法开始，使用 \"StopTrackRevisions\" 方法停止跟踪。
// 我们可以接受修订，将其合并到文档中
// 或拒绝它们，以有效地撤销提议的更改。
ASSERT_EQ(6, doc->get_Revisions()->get_Count());

// 修订的父节点是该修订涉及的 Run。Run 是一种 Inline 节点。
auto run = System::ExplicitCast<Aspose::Words::Run>(doc->get_Revisions()->idx_get(0)->get_ParentNode());

System::SharedPtr<Aspose::Words::Paragraph> firstParagraph = run->get_ParentParagraph();
System::SharedPtr<Aspose::Words::RunCollection> runs = firstParagraph->get_Runs();

ASSERT_EQ(6, runs->ToArray()->get_Length());

// 以下是可以标记 Inline 节点的五种修订类型。
// 1 -  一个 \"insert\" 修订：
// 当我们在跟踪更改时插入文本时，会产生此修订。
ASSERT_TRUE(runs->idx_get(2)->get_IsInsertRevision());

// 2 -  一个 \"format\" 修订：
// 当我们在跟踪更改时更改文本的格式时，会产生此修订。
ASSERT_TRUE(runs->idx_get(2)->get_IsFormatRevision());

// 3 -  一个 \"move from\" 修订：
// 当我们在 Microsoft Word 中突出显示文本，然后将其拖动到文档的其他位置时
// 在跟踪更改时，会出现两个修订。
// \"move from\" 修订是我们移动之前原始文本的副本。
ASSERT_TRUE(runs->idx_get(4)->get_IsMoveFromRevision());

// 4 -  一个 \"move to\" 修订：
// \"move to\" 修订是我们在文档中新位置移动的文本。
// \"Move from\" 和 \"move to\" 修订在我们执行的每个移动修订中成对出现。
// 接受移动修订会删除 "move from" 修订及其文本，
// 并保留来自 "move to" 修订的文本。
// 拒绝移动修订则相反，会保留 "move from" 修订并删除 "move to" 修订。
ASSERT_TRUE(runs->idx_get(1)->get_IsMoveToRevision());

// 5 -  一个 "delete" 修订：
// 当我们在跟踪更改时删除文本时，会出现此修订。当我们这样删除文本时，
// 它会作为修订保留在文档中，直到我们接受该修订，
// 这将永久删除文本，或拒绝该修订，后者会保留我们删除的文本在原位置。
ASSERT_TRUE(runs->idx_get(5)->get_IsDeleteRevision());
```

## 另见

* Class [Inline](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
