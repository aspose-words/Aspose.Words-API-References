---
title: "Aspose::Words::Document::get_RevisionsView 方法"
linktitle: "get_RevisionsView"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::get_RevisionsView 方法。获取或设置一个值，指示是使用文档的原始版本还是修订版本（C++）。"
type: docs
weight: 47000
url: /zh/cpp/aspose.words/document/get_revisionsview/
---
## Document::get_RevisionsView method


获取或设置一个值，指示是使用文档的原始版本还是修订版本。

```cpp
Aspose::Words::RevisionsView Aspose::Words::Document::get_RevisionsView() const
```


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

* Enum [RevisionsView](../../revisionsview/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
