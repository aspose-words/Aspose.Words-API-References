---
title: "Aspose::Words::Document::UpdateActualReferenceMarks Methode"
linktitle: "UpdateActualReferenceMarks"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::UpdateActualReferenceMarks Methode. Aktualisiert die ActualReferenceMark‑Eigenschaft aller Fußnoten und Endnoten im Dokument in C++."
type: docs
weight: 95500
url: /de/cpp/aspose.words/document/updateactualreferencemarks/
---
## Document::UpdateActualReferenceMarks method


Aktualisiert die [ActualReferenceMark](../../../aspose.words.notes/footnote/get_actualreferencemark/) Eigenschaft aller Fußnoten und Endnoten im Dokument.

```cpp
void Aspose::Words::Document::UpdateActualReferenceMarks()
```


## Beispiele



Zeigt, wie man das tatsächliche Fußnoten-Referenzzeichen erhält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

auto footnote = System::ExplicitCast<Aspose::Words::Notes::Footnote>(doc->GetChild(Aspose::Words::NodeType::Footnote, 1, true));
doc->UpdateFields();
doc->UpdateActualReferenceMarks();

ASSERT_EQ(u"1", footnote->get_ActualReferenceMark());
```

## Siehe auch

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
