---
title: "Aspose::Words::Document::get_IncludeTextboxesFootnotesEndnotesInStat metodo"
linktitle: "get_IncludeTextboxesFootnotesEndnotesInStat"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Document::get_IncludeTextboxesFootnotesEndnotesInStat metodo. Specifica se includere caselle di testo, note a piè di pagina e note finali nelle statistiche del conteggio parole in C++."
type: docs
weight: 33000
url: /it/cpp/aspose.words/document/get_includetextboxesfootnotesendnotesinstat/
---
## Document::get_IncludeTextboxesFootnotesEndnotesInStat method


Specifica se includere caselle di testo, note a piè di pagina e note finali nelle statistiche del conteggio parole.

```cpp
bool Aspose::Words::Document::get_IncludeTextboxesFootnotesEndnotesInStat()
```


## Esempi



Mostra come includere o escludere caselle di testo, note a piè di pagina e note finali dalle statistiche del conteggio parole.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Lorem ipsum");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"sit amet");

// Per impostazione predefinita l'opzione è impostata su 'false'.
doc->UpdateWordCount();
// Conteggio parole senza caselle di testo, note a piè di pagina e note finali.
ASSERT_EQ(2, doc->get_BuiltInDocumentProperties()->get_Words());

doc->set_IncludeTextboxesFootnotesEndnotesInStat(true);
doc->UpdateWordCount();
// Conteggio parole con caselle di testo, note a piè di pagina e note finali.
ASSERT_EQ(4, doc->get_BuiltInDocumentProperties()->get_Words());
```

## Vedi anche

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
