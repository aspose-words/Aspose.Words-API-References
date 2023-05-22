---
title: Aspose::Words::RevisionsView enum
linktitle: RevisionsView
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::RevisionsView enum. Allows to specify whether to work with the original or revised version of a document in C++.'
type: docs
weight: 112000
url: /cpp/aspose.words/revisionsview/
---
## RevisionsView enum


Allows to specify whether to work with the original or revised version of a document.

```cpp
enum class RevisionsView
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Original | 0 | Specifies original version of a document. |
| Final | 1 | Specifies revised version of a document. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
