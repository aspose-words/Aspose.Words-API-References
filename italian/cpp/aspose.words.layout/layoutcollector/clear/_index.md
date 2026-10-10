---
title: "Aspose::Words::Layout::LayoutCollector::Clear metodo"
linktitle: "Cancella"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Layout::LayoutCollector::Clear metodo. Cancella tutti i dati di layout raccolti. Chiama questo metodo dopo che il documento è stato aggiornato manualmente o il layout è stato ricostruito in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.layout/layoutcollector/clear/
---
## LayoutCollector::Clear method


Cancella tutti i dati di layout raccolti. Chiama questo metodo dopo che il documento è stato aggiornato manualmente, o il layout è stato ricostruito.

```cpp
void Aspose::Words::Layout::LayoutCollector::Clear()
```


## Esempi



Mostra come visualizzare gli intervalli di pagine che un nodo occupa.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto layoutCollector = System::MakeObject<Aspose::Words::Layout::LayoutCollector>(doc);

// Chiama il metodo "GetNumPagesSpanned" per contare quante pagine occupa il contenuto del nostro documento.
// Poiché il documento è vuoto, quel numero di pagine è attualmente zero.
ASPOSE_ASSERT_EQ(doc, layoutCollector->get_Document());
ASSERT_EQ(0, layoutCollector->GetNumPagesSpanned(doc));

// Popola il documento con 5 pagine di contenuto.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakEvenPage);
builder->Write(u"Section 2");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// Prima del layout collector, dobbiamo chiamare il metodo "UpdatePageLayout" per fornirci
// una cifra accurata per qualsiasi metrica relativa al layout, come il conteggio delle pagine.
ASSERT_EQ(0, layoutCollector->GetNumPagesSpanned(doc));

layoutCollector->Clear();
doc->UpdatePageLayout();

ASSERT_EQ(5, layoutCollector->GetNumPagesSpanned(doc));

// Possiamo vedere i numeri delle pagine di inizio e fine di qualsiasi nodo e le loro estensioni complessive di pagina.
System::SharedPtr<Aspose::Words::NodeCollection> nodes = doc->GetChildNodes(Aspose::Words::NodeType::Any, true);
for (auto&& node : System::IterateOver(nodes))
{
    std::cout << System::String::Format(u"->  NodeType.{0}: ", node->get_NodeType()) << std::endl;
    std::cout << (System::String::Format(u"\tStarts on page {0}, ends on page {1},", layoutCollector->GetStartPageIndex(node), layoutCollector->GetEndPageIndex(node)) + System::String::Format(u" spanning {0} pages.", layoutCollector->GetNumPagesSpanned(node))) << std::endl;
}

// Possiamo iterare le entità di layout usando un LayoutEnumerator.
auto layoutEnumerator = System::MakeObject<Aspose::Words::Layout::LayoutEnumerator>(doc);

ASSERT_EQ(Aspose::Words::Layout::LayoutEntityType::Page, layoutEnumerator->get_Type());

// Il LayoutEnumerator può attraversare la raccolta di entità di layout come un albero.
// Possiamo anche applicarlo all'entità di layout corrispondente di qualsiasi nodo.
layoutEnumerator->set_Current(layoutCollector->GetEntity(doc->GetChild(Aspose::Words::NodeType::Paragraph, 1, true)));

ASSERT_EQ(Aspose::Words::Layout::LayoutEntityType::Span, layoutEnumerator->get_Type());
ASSERT_EQ(u"¶", layoutEnumerator->get_Text());
```

## Vedi anche

* Class [LayoutCollector](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
