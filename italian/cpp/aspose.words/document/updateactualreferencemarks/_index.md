---
title: "Aspose::Words::Document::UpdateActualReferenceMarks metodo"
linktitle: "UpdateActualReferenceMarks"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Document::UpdateActualReferenceMarks metodo. Aggiorna la proprietà ActualReferenceMark di tutte le note a piè di pagina e di chiusura nel documento in C++."
type: docs
weight: 95500
url: /it/cpp/aspose.words/document/updateactualreferencemarks/
---
## Document::UpdateActualReferenceMarks method


Aggiorna la proprietà [ActualReferenceMark](../../../aspose.words.notes/footnote/get_actualreferencemark/) di tutte le note a piè di pagina e di chiusura nel documento.

```cpp
void Aspose::Words::Document::UpdateActualReferenceMarks()
```


## Esempi



Mostra come ottenere il segno di riferimento effettivo della nota a piè di pagina.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

auto footnote = System::ExplicitCast<Aspose::Words::Notes::Footnote>(doc->GetChild(Aspose::Words::NodeType::Footnote, 1, true));
doc->UpdateFields();
doc->UpdateActualReferenceMarks();

ASSERT_EQ(u"1", footnote->get_ActualReferenceMark());
```

## Vedi anche

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
