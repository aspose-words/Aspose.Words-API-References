---
title: Aspose::Words::Document::set_RevisionsView method
linktitle: set_RevisionsView
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document::set_RevisionsView method. Sets a value indicating whether to work with the original or revised version of a document in C++.'
type: docs
weight: 167000
url: /cpp/aspose.words/document/set_revisionsview/
---
## Document::set_RevisionsView method


Sets a value indicating whether to work with the original or revised version of a document.

```cpp
void Aspose::Words::Document::set_RevisionsView(Aspose::Words::RevisionsView value)
```

## Remarks

 The default value is [Aspose.Words.RevisionsView.Original](../../revisionsview/). 
## Examples


Shows how to switch between the revised and the original view of a document.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Revisions at list levels.docx"));
doc->UpdateListLabels();

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();
ASSERT_EQ(u"1.", paragraphs->idx_get(0)->get_ListLabel()->get_LabelString());
ASSERT_EQ(u"a.", paragraphs->idx_get(1)->get_ListLabel()->get_LabelString());
ASSERT_EQ(System::String::Empty, paragraphs->idx_get(2)->get_ListLabel()->get_LabelString());

// View the document object as if all the revisions are accepted. Currently supports list labels.
doc->set_RevisionsView(RevisionsView::Final);

ASSERT_EQ(System::String::Empty, paragraphs->idx_get(0)->get_ListLabel()->get_LabelString());
ASSERT_EQ(u"1.", paragraphs->idx_get(1)->get_ListLabel()->get_LabelString());
ASSERT_EQ(u"a.", paragraphs->idx_get(2)->get_ListLabel()->get_LabelString());
```
## See Also

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
