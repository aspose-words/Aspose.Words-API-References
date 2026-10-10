---
title: "Metodo Aspose::Words::Node::GetText"
linktitle: "GetText"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Node::GetText. Ottiene il testo di questo nodo e di tutti i suoi figli in C++."
type: docs
weight: 15000
url: /it/cpp/aspose.words/node/gettext/
---
## Node::GetText method


Ottiene il testo di questo nodo e di tutti i suoi figli.

```cpp
virtual System::String Aspose::Words::Node::GetText()
```

## Note


La stringa restituita include tutti i caratteri di controllo e speciali come descritti in [ControlChar](../../controlchar/).

## Esempi



Mostra come utilizzare i caratteri di controllo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci paragrafi con testo usando DocumentBuilder.
builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

// Convertire il documento in forma testuale rivela che i caratteri di controllo
// rappresentano alcuni degli elementi strutturali del documento, come le interruzioni di pagina.
ASSERT_EQ(System::String::Format(u"Hello world!{0}", Aspose::Words::ControlChar::Cr()) + System::String::Format(u"Hello again!{0}", Aspose::Words::ControlChar::Cr()) + Aspose::Words::ControlChar::PageBreak(), doc->GetText());

// Durante la conversione di un documento in forma stringa,
// possiamo omettere alcuni dei caratteri di controllo con il metodo Trim.
ASSERT_EQ(System::String::Format(u"Hello world!{0}", Aspose::Words::ControlChar::Cr()) + u"Hello again!", doc->GetText().Trim());
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

* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
