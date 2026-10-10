---
title: "Aspose::Words::RevisionsView enum"
linktitle: "RevisionsView"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::RevisionsView 枚举。允许指定在 C++ 中是使用文档的原始版本还是修订版本。"
type: docs
weight: 112000
url: /zh/cpp/aspose.words/revisionsview/
---
## RevisionsView enum


允许指定是使用文档的原始版本还是修订版本。

```cpp
enum class RevisionsView
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| 原始 | 0 | 指定文档的原始版本。 |
| 修订版 | 1 | 指定文档的修订版本。 |


## 示例



展示如何在文档的修订视图和原始视图之间切换。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions at list levels.docx");
doc->UpdateListLabels();

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();
ASSERT_EQ(u"1.", paragraphs->idx_get(0)->get_ListLabel()->get_LabelString());
ASSERT_EQ(u"a.", paragraphs->idx_get(1)->get_ListLabel()->get_LabelString());
ASSERT_EQ(System::String::Empty, paragraphs->idx_get(2)->get_ListLabel()->get_LabelString());

// 将文档对象视为已接受所有修订的状态。目前支持列表标签。
doc->set_RevisionsView(Aspose::Words::RevisionsView::Final);

ASSERT_EQ(System::String::Empty, paragraphs->idx_get(0)->get_ListLabel()->get_LabelString());
ASSERT_EQ(u"1.", paragraphs->idx_get(1)->get_ListLabel()->get_LabelString());
ASSERT_EQ(u"a.", paragraphs->idx_get(2)->get_ListLabel()->get_LabelString());
```

## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
