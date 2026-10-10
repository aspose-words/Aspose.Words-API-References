---
title: "Aspose::Words::Section::AppendContent metodo"
linktitle: "AppendContent"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Section::AppendContent metodo. Inserisce una copia del contenuto della sezione di origine alla fine di questa sezione in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words/section/appendcontent/
---
## Section::AppendContent method


Inserisce una copia del contenuto della sezione di origine alla fine di questa sezione.

```cpp
void Aspose::Words::Section::AppendContent(const System::SharedPtr<Aspose::Words::Section> &sourceSection)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| sourceSection | const System::SharedPtr\<Aspose::Words::Section\>\& | La sezione da cui copiare il contenuto. |
## Note


Solo il contenuto di [Body](../get_body/) della sezione di origine viene copiato, l'impostazione della pagina, intestazioni e piè di pagina non vengono copiati.

I nodi vengono importati automaticamente se la sezione di origine appartiene a un documento diverso.

Nessuna nuova sezione viene creata nel documento di destinazione.

## Esempi



Mostra come aggiungere il contenuto di una sezione a un'altra sezione.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 3");

System::SharedPtr<Aspose::Words::Section> section = doc->get_Sections()->idx_get(2);

ASSERT_EQ(System::String(u"Section 3") + Aspose::Words::ControlChar::SectionBreak(), section->GetText());

// Inserisci il contenuto della prima sezione all'inizio della terza sezione.
System::SharedPtr<Aspose::Words::Section> sectionToPrepend = doc->get_Sections()->idx_get(0);
section->PrependContent(sectionToPrepend);

// Inserisci il contenuto della seconda sezione alla fine della terza sezione.
System::SharedPtr<Aspose::Words::Section> sectionToAppend = doc->get_Sections()->idx_get(1);
section->AppendContent(sectionToAppend);

// I metodi \"PrependContent\" e \"AppendContent\" non hanno creato nuove sezioni.
ASSERT_EQ(3, doc->get_Sections()->get_Count());
ASSERT_EQ(System::String(u"Section 1") + Aspose::Words::ControlChar::ParagraphBreak() + u"Section 3" + Aspose::Words::ControlChar::ParagraphBreak() + u"Section 2" + Aspose::Words::ControlChar::SectionBreak(), section->GetText());
```

## Vedi anche

* Class [Section](../)
* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
