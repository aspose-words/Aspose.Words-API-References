---
title: "Metodo Aspose::Words::Document::get_Sections"
linktitle: "get_Sections"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Document::get_Sections. Restituisce una collezione che rappresenta tutte le sezioni del documento in C++."
type: docs
weight: 48000
url: /it/cpp/aspose.words/document/get_sections/
---
## Document::get_Sections method


Restituisce una raccolta che rappresenta tutte le sezioni del documento.

```cpp
System::SharedPtr<Aspose::Words::SectionCollection> Aspose::Words::Document::get_Sections()
```


## Esempi



Mostra come specificare come una nuova sezione si separa dalla precedente.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"This text is in section 1.");

// I tipi di interruzione di sezione determinano come una nuova sezione si separa dalla sezione precedente.
// Di seguito sono riportati cinque tipi di interruzioni di sezione.
// 1 -  Avvia la sezione successiva su una nuova pagina:
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Writeln(u"This text is in section 2.");

ASSERT_EQ(Aspose::Words::SectionStart::NewPage, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_SectionStart());

// 2 -  Avvia la sezione successiva sulla pagina corrente:
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakContinuous);
builder->Writeln(u"This text is in section 3.");

ASSERT_EQ(Aspose::Words::SectionStart::Continuous, doc->get_Sections()->idx_get(2)->get_PageSetup()->get_SectionStart());

// 3 -  Avvia la sezione successiva su una nuova pagina pari:
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakEvenPage);
builder->Writeln(u"This text is in section 4.");

ASSERT_EQ(Aspose::Words::SectionStart::EvenPage, doc->get_Sections()->idx_get(3)->get_PageSetup()->get_SectionStart());

// 4 -  Avvia la sezione successiva su una nuova pagina dispari:
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakOddPage);
builder->Writeln(u"This text is in section 5.");

ASSERT_EQ(Aspose::Words::SectionStart::OddPage, doc->get_Sections()->idx_get(4)->get_PageSetup()->get_SectionStart());

// 5 -  Avvia la sezione successiva su una nuova colonna:
System::SharedPtr<Aspose::Words::TextColumnCollection> columns = builder->get_PageSetup()->get_TextColumns();
columns->SetCount(2);

builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewColumn);
builder->Writeln(u"This text is in section 6.");

ASSERT_EQ(Aspose::Words::SectionStart::NewColumn, doc->get_Sections()->idx_get(5)->get_PageSetup()->get_SectionStart());

doc->Save(get_ArtifactsDir() + u"PageSetup.SetSectionStart.docx");
```


Mostra come aggiungere e rimuovere sezioni in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");

ASSERT_EQ(u"Section 1\x000c" u"Section 2", doc->GetText().Trim());

// Elimina la prima sezione dal documento.
doc->get_Sections()->RemoveAt(0);

ASSERT_EQ(u"Section 2", doc->GetText().Trim());

// Aggiungi una copia di quella che è ora la prima sezione alla fine del documento.
int32_t lastSectionIdx = doc->get_Sections()->get_Count() - 1;
System::SharedPtr<Aspose::Words::Section> newSection = doc->get_Sections()->idx_get(lastSectionIdx)->Clone();
doc->get_Sections()->Add(newSection);

ASSERT_EQ(u"Section 2\x000c" u"Section 2", doc->GetText().Trim());
```

## Vedi anche

* Class [SectionCollection](../../sectioncollection/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
