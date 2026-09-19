---
title: "Aspose::Words::Layout::LayoutCollector::GetEntity metodo"
linktitle: "GetEntity"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Layout::LayoutCollector::GetEntity metodo. Restituisce una posizione opaca del LayoutEnumerator che corrisponde al nodo specificato. È possibile utilizzare il valore restituito come argomento per Current dato che il documento enumerato e il documento del nodo sono gli stessi in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.layout/layoutcollector/getentity/
---
## LayoutCollector::GetEntity method


Restituisce una posizione opaca del [LayoutEnumerator](../../layoutenumerator/) che corrisponde al nodo specificato. È possibile utilizzare il valore restituito come argomento per [Current](../../layoutenumerator/get_current/) dato che il documento enumerato e il documento del nodo sono gli stessi.

```cpp
System::SharedPtr<System::Object> Aspose::Words::Layout::LayoutCollector::GetEntity(const System::SharedPtr<Aspose::Words::Node> &node)
```

## Note


Questo metodo funziona solo per i nodi [Paragraph](../../../aspose.words/paragraph/), così come per i nodi inline indivisibili, ad es. [BookmarkStart](../../../aspose.words/bookmarkstart/) o [Shape](../../../aspose.words.drawing/shape/). Non funziona per i nodi [Run](../../../aspose.words/run/), [Cell](../../../aspose.words.tables/cell/)[Row](../../../aspose.words.tables/row/) o [Table](../../../aspose.words.tables/table/) e per i nodi all'interno di intestazione/piè di pagina.

Nota che l'entità restituita per un nodo [Paragraph](../../../aspose.words/paragraph/) è uno span di interruzione di paragrafo. Usa il metodo appropriato per ascendere alla riga padre.

Se hai bisogno di navigare a un [Run](../../../aspose.words/run/) di testo, puoi inserire un segnalibro subito prima di esso e poi navigare al segnalibro.

Se hai bisogno di navigare a un nodo [Cell](../../../aspose.words.tables/cell/), puoi spostarti a un nodo [Paragraph](../../../aspose.words/paragraph/) in questa cella e poi ascendere a un'entità padre. Lo stesso approccio può essere usato per i nodi [Row](../../../aspose.words.tables/row/) e [Table](../../../aspose.words.tables/table/).

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

* Class [Node](../../../aspose.words/node/)
* Class [LayoutCollector](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
