---
title: "Aspose::Words::Layout::LayoutCollector classe"
linktitle: "LayoutCollector"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Layout::LayoutCollector class. Questa classe consente di calcolare i numeri di pagina dei nodi del documento. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 1000
url: /it/cpp/aspose.words.layout/layoutcollector/
---
## LayoutCollector class


Questa classe consente di calcolare i numeri di pagina dei nodi del documento. Per saperne di più, visita l'articolo di documentazione [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/).

```cpp
class LayoutCollector : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Clear](./clear/)() | Cancella tutti i dati di layout raccolti. Chiama questo metodo dopo che il documento è stato aggiornato manualmente, o il layout è stato ricostruito. |
| [get_Document](./get_document/)() const | Ottiene o imposta il documento a cui è collegata questa istanza del raccoglitore. |
| [GetEndPageIndex](./getendpageindex/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ottiene l'indice basato su uno della pagina in cui il nodo termina. Restituisce 0 se il nodo non può essere mappato a una pagina. |
| [GetEntity](./getentity/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Restituisce una posizione opaca del [LayoutEnumerator](../layoutenumerator/) che corrisponde al nodo specificato. Puoi usare il valore restituito come argomento per [Current](../layoutenumerator/get_current/) dato che il documento enumerato e il documento del nodo sono gli stessi. |
| [GetNumPagesSpanned](./getnumpagesspanned/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ottiene il numero di pagine che il nodo specificato occupa. 0 se il nodo è all'interno di una singola pagina. Questo è lo stesso di [GetEndPageIndex()](../) - [GetStartPageIndex()](../). |
| [GetStartPageIndex](./getstartpageindex/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ottiene l'indice basato su uno della pagina in cui il nodo inizia. Restituisce 0 se il nodo non può essere mappato a una pagina. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LayoutCollector](./layoutcollector/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | Inizializza un'istanza di questa classe. |
| [set_Document](./set_document/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | Setter per [Aspose::Words::Layout::LayoutCollector::get_Document](./get_document/). |
| static [Type](./type/)() |  |
## Note


Quando crei un [LayoutCollector](./) e specifichi un oggetto [Document](../../aspose.words/document/) a cui collegarlo, il raccoglitore registrerà la mappatura dei nodi del documento agli oggetti di layout quando il documento viene formattato in pagine.

Potrai scoprire su quale pagina si trova un particolare nodo del documento (ad es. run, paragrafo o cella di tabella) utilizzando i metodi [GetStartPageIndex()](../), [GetEndPageIndex()](../) e [GetNumPagesSpanned()](../). Questi metodi costruiscono automaticamente il modello di layout della pagina del documento e aggiornano i campi se necessario.

Quando non hai più bisogno di raccogliere informazioni di layout, è consigliabile impostare la proprietà [Document](./get_document/) su **null** per evitare la raccolta non necessaria di ulteriori mappature di layout.

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

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
