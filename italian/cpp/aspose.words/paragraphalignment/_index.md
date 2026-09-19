---
title: "Aspose::Words::ParagraphAlignment enum"
linktitle: "ParagraphAlignment"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::ParagraphAlignment enum. Specifica l'allineamento del testo in un paragrafo in C++."
type: docs
weight: 110000
url: /it/cpp/aspose.words/paragraphalignment/
---
## ParagraphAlignment enum


Specifica l'allineamento del testo in un paragrafo.

```cpp
enum class ParagraphAlignment
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Sinistra | 0 | Il testo è allineato a sinistra. |
| Centro | 1 | Il testo è centrato orizzontalmente. |
| Destra | 2 | Il testo è allineato a destra. |
| Giustifica | 3 | Il testo è allineato sia a sinistra che a destra. |
| Distributed | 4 | Il testo è distribuito uniformemente. |
| ArabicMediumKashida | 5 | Solo arabo. La lunghezza del Kashida per il testo è estesa a una lunghezza media determinata dal consumatore. |
| ArabicHighKashida | 7 | Solo arabo. La lunghezza del Kashida per il testo è estesa alla sua massima lunghezza possibile. |
| ArabicLowKashida | 8 | Solo arabo. La lunghezza del Kashida per il testo è estesa a una lunghezza leggermente più lunga. |
| ThaiDistributed | 9 | Solo tailandese. Il testo è giustificato con un'ottimizzazione per il tailandese. |
| MathElementCenterAsGroup | 10 | L'unico elemento [Math](../../aspose.words.math/) in una riga, allineato come 'Centered As Group'. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
