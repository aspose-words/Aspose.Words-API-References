---
title: "Aspose::Words::Document::EnsureMinimum metodo"
linktitle: "EnsureMinimum"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Document::EnsureMinimum metodo. Se il documento non contiene sezioni, crea una sezione con un paragrafo in C++."
type: docs
weight: 10000
url: /it/cpp/aspose.words/document/ensureminimum/
---
## Document::EnsureMinimum method


Se il documento non contiene sezioni, crea una sezione con un paragrafo.

```cpp
void Aspose::Words::Document::EnsureMinimum()
```


## Esempi



Mostra come garantire che un documento contenga il set minimo di nodi necessario per modificare il suo contenuto.
```cpp
// Un documento appena creato contiene una sezione figlia, che include un corpo figlio e un paragrafo figlio.
// Possiamo modificare il contenuto del corpo del documento aggiungendo nodi come Run o Forme in linea a quel paragrafo.
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::NodeCollection> nodes = doc->GetChildNodes(Aspose::Words::NodeType::Any, true);

ASSERT_EQ(Aspose::Words::NodeType::Section, nodes->idx_get(0)->get_NodeType());
ASPOSE_ASSERT_EQ(doc, nodes->idx_get(0)->get_ParentNode());

ASSERT_EQ(Aspose::Words::NodeType::Body, nodes->idx_get(1)->get_NodeType());
ASPOSE_ASSERT_EQ(nodes->idx_get(0), nodes->idx_get(1)->get_ParentNode());

ASSERT_EQ(Aspose::Words::NodeType::Paragraph, nodes->idx_get(2)->get_NodeType());
ASPOSE_ASSERT_EQ(nodes->idx_get(1), nodes->idx_get(2)->get_ParentNode());

// Questo è il set minimo di nodi di cui abbiamo bisogno per poter modificare il documento.
// Non saremo più in grado di modificare il documento se ne rimuoviamo qualcuno.
doc->RemoveAllChildren();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Chiama questo metodo per assicurarti che il documento abbia almeno quei tre nodi così da poterlo modificare nuovamente.
doc->EnsureMinimum();

ASSERT_EQ(Aspose::Words::NodeType::Section, nodes->idx_get(0)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Body, nodes->idx_get(1)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, nodes->idx_get(2)->get_NodeType());

(System::ExplicitCast<Aspose::Words::Paragraph>(nodes->idx_get(2)))->get_Runs()->Add(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```

## Vedi anche

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
