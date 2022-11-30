---
title: get_RevisionsView
second_title: Aspose.Words for C++ API Reference
description: Gets or sets a value indicating whether to work with the original or revised version of a document.
type: docs
weight: 560
url: /cpp/aspose.words/document/get_revisionsview/
---
## Document::get_RevisionsView method


Gets or sets a value indicating whether to work with the original or revised version of a document.

```cpp
Aspose::Words::RevisionsView Aspose::Words::Document::get_RevisionsView() const
```


## Examples



Shows how to switch between the revised and the original view of a document. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Revisions at list levels.docx");
doc->UpdateListLabels();

SharedPtr<ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();
ASSERT_EQ(u"1.", paragraphs->idx_get(0)->get_ListLabel()->get_LabelString());
ASSERT_EQ(u"a.", paragraphs->idx_get(1)->get_ListLabel()->get_LabelString());
ASSERT_EQ(String::Empty, paragraphs->idx_get(2)->get_ListLabel()->get_LabelString());

// View the document object as if all the revisions are accepted. Currently supports list labels.
doc->set_RevisionsView(RevisionsView::Final);

ASSERT_EQ(String::Empty, paragraphs->idx_get(0)->get_ListLabel()->get_LabelString());
ASSERT_EQ(u"1.", paragraphs->idx_get(1)->get_ListLabel()->get_LabelString());
ASSERT_EQ(u"a.", paragraphs->idx_get(2)->get_ListLabel()->get_LabelString());
```

## See Also

* Enum [RevisionsView](../../revisionsview/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
