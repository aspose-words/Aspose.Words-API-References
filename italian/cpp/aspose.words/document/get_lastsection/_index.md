---
title: "Metodo Aspose::Words::Document::get_LastSection"
linktitle: "get_LastSection"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Document::get_LastSection. Ottiene l'ultima sezione del documento in C++."
type: docs
weight: 35000
url: /it/cpp/aspose.words/document/get_lastsection/
---
## Document::get_LastSection method


Ottiene l'ultima sezione del documento.

```cpp
System::SharedPtr<Aspose::Words::Section> Aspose::Words::Document::get_LastSection()
```


## Esempi



Mostra come creare una nuova sezione con un document builder.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Un documento vuoto contiene una sezione per impostazione predefinita,
// che contiene nodi figlio che possiamo modificare.
ASSERT_EQ(1, doc->get_Sections()->get_Count());

// Usa un document builder per aggiungere testo alla prima sezione.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Crea una seconda sezione inserendo un'interruzione di sezione.
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

ASSERT_EQ(2, doc->get_Sections()->get_Count());

// Ogni sezione ha le proprie impostazioni di layout di pagina.
// Possiamo dividere il testo nella seconda sezione in due colonne.
// Questo non influenzerà il testo nella prima sezione.
doc->get_LastSection()->get_PageSetup()->get_TextColumns()->SetCount(2);
builder->Writeln(u"Column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Column 2.");

ASSERT_EQ(1, doc->get_FirstSection()->get_PageSetup()->get_TextColumns()->get_Count());
ASSERT_EQ(2, doc->get_LastSection()->get_PageSetup()->get_TextColumns()->get_Count());

doc->Save(get_ArtifactsDir() + u"Section.Create.docx");
```

## Vedi anche

* Class [Section](../../section/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
