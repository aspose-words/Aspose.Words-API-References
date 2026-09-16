---
title: "Aspose::Words::ParagraphCollection::idx_get 方法"
linktitle: "idx_get"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ParagraphCollection::idx_get 方法。检索 C++ 中给定索引处的 Paragraph。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words/paragraphcollection/idx_get/
---
## ParagraphCollection::idx_get method


检索给定索引处的 [Paragraph](../../paragraph/)。

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::ParagraphCollection::idx_get(int32_t index)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| index | int32_t | 集合中的索引。 |
## 备注


索引从零开始。

允许使用负索引，并表示从集合的末尾访问。例如 -1 表示最后一个项目，-2 表示倒数第二个，依此类推。

如果索引大于或等于列表中的项目数，则返回空引用。

如果索引为负且其绝对值大于列表中的项目数，则返回空引用。

## 示例



展示如何检查段落是否为移动修订。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

// 本文档包含“Move”修订，当我们使用光标突出显示文本时会出现这些修订，
// 然后将其拖动以移动到另一个位置
// 在 Microsoft Word 中通过 "Review" -> "Track changes" 跟踪修订。
ASSERT_EQ(6, doc->get_Revisions()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Revision>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Revision> r)>>([](System::SharedPtr<Aspose::Words::Revision> r) -> bool
{
    return r->get_RevisionType() == Aspose::Words::RevisionType::Moving;
}))));

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

// 移动修订由一对 "Move from" 和 "Move to" 修订组成。
// 这些修订是文档的潜在更改，我们可以接受或拒绝它们。
// 在我们接受/拒绝移动修订之前，文档
// 必须跟踪文本的出发和到达位置。
// 第二段和第四段定义了这种修订，因此两者内容相同。
ASSERT_EQ(paragraphs->idx_get(1)->GetText(), paragraphs->idx_get(3)->GetText());

// "Move from" 修订是我们拖动文本的段落。
// 如果我们接受该修订，此段落将消失，
// 而另一个将保留且不再是修订。
ASSERT_TRUE(paragraphs->idx_get(1)->get_IsMoveFromRevision());

// "Move to" 修订是我们将文本拖动到的段落。
// 如果我们拒绝该修订，此段落将消失，而另一个将保留。
ASSERT_TRUE(paragraphs->idx_get(3)->get_IsMoveToRevision());
```

## 另见

* Class [Paragraph](../../paragraph/)
* Class [ParagraphCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
