---
title: "Aspose::Words::Paragraph::Paragraph costruttore"
linktitle: "Paragraph"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Paragraph::Paragraph costruttore. Inizializza una nuova istanza della classe Paragraph in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words/paragraph/paragraph/
---
## Paragraph::Paragraph constructor


Inizializza una nuova istanza della classe [Paragraph](../).

```cpp
Aspose::Words::Paragraph::Paragraph(const System::SharedPtr<Aspose::Words::DocumentBase> &doc)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Il documento proprietario. |
## Note


Quando il [Paragraph](../) viene creato, appartiene al documento specificato, ma non è ancora parte del documento e [ParentNode](../../node/get_parentnode/) è **null**.

Per aggiungere il [Paragraph](../) al documento, usa [InsertAfter1()</see> o <see cref=\"Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)\">InsertBefore1()](../) sulla storia in cui desideri inserire il paragrafo.

## Esempi



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

* Class [DocumentBase](../../documentbase/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
