---
title: "Aspose::Words::RevisionsView enum"
linktitle: "RevisionsView"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::RevisionsView enum. Tillåter att ange om man ska arbeta med original- eller reviderad version av ett dokument i C++."
type: docs
weight: 112000
url: /sv/cpp/aspose.words/revisionsview/
---
## RevisionsView enum


Tillåter att ange om man ska arbeta med original- eller reviderad version av ett dokument.

```cpp
enum class RevisionsView
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Original | 0 | Anger originalversionen av ett dokument. |
| Slutlig | 1 | Anger reviderad version av ett dokument. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
