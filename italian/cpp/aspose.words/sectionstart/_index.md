---
title: "Aspose::Words::SectionStart enum"
linktitle: "SectionStart"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::SectionStart enum. Il tipo di interruzione all'inizio della sezione in C++."
type: docs
weight: 116000
url: /it/cpp/aspose.words/sectionstart/
---
## SectionStart enum


Il tipo di interruzione all'inizio della sezione.

```cpp
enum class SectionStart
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Continuous | 0 | La nuova sezione inizia nella stessa pagina della sezione precedente. |
| NewColumn | 1 | La sezione inizia da una nuova colonna. |
| NewPage | 2 | La sezione inizia da una nuova pagina. |
| EvenPage | 3 | La sezione inizia su una nuova pagina pari. |
| OddPage | 4 | La sezione inizia su una nuova pagina dispari. |


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


Mostra come costruire manualmente un documento Aspose.Words.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Un documento vuoto contiene una sezione, un corpo e un paragrafo.
// Chiama il metodo "RemoveAllChildren" per rimuovere tutti quei nodi,
// e otterrai un nodo documento senza figli.
doc->RemoveAllChildren();

// Questo documento ora non ha nodi figli compositi a cui possiamo aggiungere contenuti.
// Se desideriamo modificarlo, dovremo ripopolare la sua collezione di nodi.
// Per prima cosa, crea una nuova sezione, quindi aggiungila come figlio al nodo radice del documento.
auto section = System::MakeObject<Aspose::Words::Section>(doc);
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(section);

// Imposta alcune proprietà di configurazione della pagina per la sezione.
section->get_PageSetup()->set_SectionStart(Aspose::Words::SectionStart::NewPage);
section->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Letter);

// Una sezione ha bisogno di un corpo, che conterrà e visualizzerà tutti i suoi contenuti
// sulla pagina tra l'intestazione e il piè di pagina della sezione.
auto body = System::MakeObject<Aspose::Words::Body>(doc);
section->AppendChild<System::SharedPtr<Aspose::Words::Body>>(body);

// Crea un paragrafo, imposta alcune proprietà di formattazione e quindi aggiungilo come figlio al corpo.
auto para = System::MakeObject<Aspose::Words::Paragraph>(doc);

para->get_ParagraphFormat()->set_StyleName(u"Heading 1");
para->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

body->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(para);

// Infine, aggiungi del contenuto al documento. Crea un run,
// imposta il suo aspetto e i suoi contenuti, e quindi aggiungilo come figlio al paragrafo.
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"Hello World!");
run->get_Font()->set_Color(System::Drawing::Color::get_Red());
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

ASSERT_EQ(u"Hello World!", doc->GetText().Trim());

doc->Save(get_ArtifactsDir() + u"Section.CreateManually.docx");
```

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
