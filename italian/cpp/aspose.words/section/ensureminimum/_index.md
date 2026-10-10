---
title: "Aspose::Words::Section::EnsureMinimum metodo"
linktitle: "EnsureMinimum"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Section::EnsureMinimum metodo. Garantisce che la sezione abbia un Body con un Paragraph in C++."
type: docs
weight: 9000
url: /it/cpp/aspose.words/section/ensureminimum/
---
## Section::EnsureMinimum method


Garantisce che la sezione abbia un [Body](../get_body/) con un [Paragraph](../../paragraph/).

```cpp
void Aspose::Words::Section::EnsureMinimum()
```


## Esempi



Mostra come preparare un nuovo nodo sezione per la modifica.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Un documento vuoto contiene una sezione, che ha un body, che a sua volta ha un paragrafo.
// Possiamo aggiungere contenuti a questo documento aggiungendo elementi come sequenze di testo, forme o tabelle a quel paragrafo.
ASSERT_EQ(Aspose::Words::NodeType::Section, doc->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Body, doc->get_Sections()->idx_get(0)->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, doc->get_Sections()->idx_get(0)->get_Body()->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());

// Se aggiungiamo una nuova sezione in questo modo, non avrà un body, né altri nodi figli.
doc->get_Sections()->Add(System::MakeObject<Aspose::Words::Section>(doc));

ASSERT_EQ(0, doc->get_Sections()->idx_get(1)->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Esegui il metodo \"EnsureMinimum\" per aggiungere un body e un paragrafo a questa sezione per iniziare a modificarla.
doc->get_LastSection()->EnsureMinimum();

ASSERT_EQ(Aspose::Words::NodeType::Body, doc->get_Sections()->idx_get(1)->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, doc->get_Sections()->idx_get(1)->get_Body()->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());

doc->get_Sections()->idx_get(0)->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## Vedi anche

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
