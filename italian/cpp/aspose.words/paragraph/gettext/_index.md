---
title: "Aspose::Words::Paragraph::GetText method"
linktitle: "GetText"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Paragraph::GetText metodo. Ottiene il testo di questo paragrafo includendo il carattere di fine paragrafo in C++."
type: docs
weight: 27000
url: /it/cpp/aspose.words/paragraph/gettext/
---
## Paragraph::GetText method


Ottiene il testo di questo paragrafo includendo il carattere di fine paragrafo.

```cpp
System::String Aspose::Words::Paragraph::GetText() override
```

## Note


Il testo di tutti i nodi figlio viene concatenato e il carattere di fine paragrafo viene aggiunto come segue:

* If the paragraph is the last paragraph of [Body](../../body/), then [SectionBreak](../../controlchar/sectionbreak/) (\x000c) is appended.
* If the paragraph is the last paragraph of [Cell](../../../aspose.words.tables/cell/), then [Cell](../../controlchar/cell/) (\x0007) is appended.
* For all other paragraphs [ParagraphBreak](../../controlchar/paragraphbreak/) (\r) is appended.



La stringa restituita include tutti i caratteri di controllo e speciali come descritti in [ControlChar](../../controlchar/).

## Esempi



Mostra come aggiungere, aggiornare ed eliminare i nodi figlio in una collezione di figli di un [CompositeNode](../../compositenode/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Un documento vuoto, per impostazione predefinita, ha un paragrafo.
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_Paragraphs()->get_Count());

// I nodi compositi, come il nostro paragrafo, possono contenere altri nodi compositi e inline come figli.
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();
auto paragraphText = System::MakeObject<Aspose::Words::Run>(doc, u"Initial text. ");
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(paragraphText);

// Crea altri tre nodi run.
auto run1 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 1. ");
auto run2 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 2. ");
auto run3 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 3. ");

// Il corpo del documento non visualizzerà questi run finché non li inseriamo in un nodo composito
// che è esso stesso parte dell'albero dei nodi del documento, come abbiamo fatto con il primo run.
// Possiamo determinare dove il contenuto testuale dei nodi che inseriamo
// appare nel documento specificando una posizione di inserimento relativa a un altro nodo nel paragrafo.
ASSERT_EQ(u"Initial text.", paragraph->GetText().Trim());

// Inserisci il secondo run nel paragrafo davanti al run iniziale.
paragraph->InsertBefore<System::SharedPtr<Aspose::Words::Run>>(run2, paragraphText);

ASSERT_EQ(u"Run 2. Initial text.", paragraph->GetText().Trim());

// Inserisci il terzo run dopo il run iniziale.
paragraph->InsertAfter<System::SharedPtr<Aspose::Words::Run>>(run3, paragraphText);

ASSERT_EQ(u"Run 2. Initial text. Run 3.", paragraph->GetText().Trim());

// Inserisci il primo run all'inizio della collezione di nodi figlio del paragrafo.
paragraph->PrependChild<System::SharedPtr<Aspose::Words::Run>>(run1);

ASSERT_EQ(u"Run 1. Run 2. Initial text. Run 3.", paragraph->GetText().Trim());
ASSERT_EQ(4, paragraph->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Possiamo modificare il contenuto del run modificando ed eliminando i nodi figlio esistenti.
(System::ExplicitCast<Aspose::Words::Run>(paragraph->GetChildNodes(Aspose::Words::NodeType::Run, true)->idx_get(1)))->set_Text(u"Updated run 2. ");
paragraph->GetChildNodes(Aspose::Words::NodeType::Run, true)->Remove(paragraphText);

ASSERT_EQ(u"Run 1. Updated run 2. Run 3.", paragraph->GetText().Trim());
ASSERT_EQ(3, paragraph->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());
```

## Vedi anche

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
