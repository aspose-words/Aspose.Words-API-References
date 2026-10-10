---
title: "Aspose::Words::Document::UpdateActualReferenceMarks metod"
linktitle: "UpdateActualReferenceMarks"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Document::UpdateActualReferenceMarks metod. Uppdaterar ActualReferenceMark‑egenskapen för alla fotnoter och slutnoter i dokumentet i C++."
type: docs
weight: 95500
url: /sv/cpp/aspose.words/document/updateactualreferencemarks/
---
## Document::UpdateActualReferenceMarks method


Uppdaterar [ActualReferenceMark](../../../aspose.words.notes/footnote/get_actualreferencemark/)‑egenskapen för alla fotnoter och slutnoter i dokumentet.

```cpp
void Aspose::Words::Document::UpdateActualReferenceMarks()
```


## Exempel



Visar hur man hämtar den faktiska fotnotreferensmarkeringen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

auto footnote = System::ExplicitCast<Aspose::Words::Notes::Footnote>(doc->GetChild(Aspose::Words::NodeType::Footnote, 1, true));
doc->UpdateFields();
doc->UpdateActualReferenceMarks();

ASSERT_EQ(u"1", footnote->get_ActualReferenceMark());
```

## Se även

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
