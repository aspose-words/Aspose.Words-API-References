---
title: "Aspose::Words::Notes::Footnote::get_ActualReferenceMark metodo"
linktitle: "get_ActualReferenceMark"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Notes::Footnote::get_ActualReferenceMark metodo. Ottiene il testo effettivo del segno di riferimento visualizzato nel documento per questa nota a piè di pagina in C++."
type: docs
weight: 3834
url: /it/cpp/aspose.words.notes/footnote/get_actualreferencemark/
---
## Footnote::get_ActualReferenceMark method


Ottiene il testo effettivo del segno di riferimento visualizzato nel documento per questa nota a piè di pagina.

```cpp
System::String Aspose::Words::Notes::Footnote::get_ActualReferenceMark()
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

* Class [Footnote](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
