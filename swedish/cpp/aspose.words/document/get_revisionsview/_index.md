---
title: "Aspose::Words::Document::get_RevisionsView metod"
linktitle: "get_RevisionsView"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Document::get_RevisionsView metod. Hämtar eller anger ett värde som indikerar om man ska arbeta med original- eller reviderad version av ett dokument i C++."
type: docs
weight: 47000
url: /sv/cpp/aspose.words/document/get_revisionsview/
---
## Document::get_RevisionsView method


Hämtar eller anger ett värde som indikerar om man ska arbeta med den ursprungliga eller reviderade versionen av ett dokument.

```cpp
Aspose::Words::RevisionsView Aspose::Words::Document::get_RevisionsView() const
```


## Exempel



Visar hur man växlar mellan den reviderade och den ursprungliga vyn av ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions at list levels.docx");
doc->UpdateListLabels();

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();
ASSERT_EQ(u"1.", paragraphs->idx_get(0)->get_ListLabel()->get_LabelString());
ASSERT_EQ(u"a.", paragraphs->idx_get(1)->get_ListLabel()->get_LabelString());
ASSERT_EQ(System::String::Empty, paragraphs->idx_get(2)->get_ListLabel()->get_LabelString());

// Visa dokumentobjektet som om alla revisioner är accepterade. Stöder för närvarande listetiketter.
doc->set_RevisionsView(Aspose::Words::RevisionsView::Final);

ASSERT_EQ(System::String::Empty, paragraphs->idx_get(0)->get_ListLabel()->get_LabelString());
ASSERT_EQ(u"1.", paragraphs->idx_get(1)->get_ListLabel()->get_LabelString());
ASSERT_EQ(u"a.", paragraphs->idx_get(2)->get_ListLabel()->get_LabelString());
```

## Se även

* Enum [RevisionsView](../../revisionsview/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
