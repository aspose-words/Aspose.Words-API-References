---
title: "Classe Aspose::Words::Layout::LayoutEnumerator"
linktitle: "LayoutEnumerator"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::Layout::LayoutEnumerator. Enumera le entità di layout di pagina di un documento. È possibile utilizzare questa classe per attraversare il modello di layout di pagina. Le proprietà disponibili sono tipo, geometria, testo e indice di pagina dove l'entità è renderizzata, nonché la struttura complessiva e le relazioni. Utilizzare la combinazione di GetEntity() e Current per spostarsi all'entità che corrisponde a un nodo del documento. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.layout/layoutenumerator/
---
## LayoutEnumerator class


Enumera le entità di layout di pagina di un documento. È possibile utilizzare questa classe per attraversare il modello di layout di pagina. Le proprietà disponibili sono tipo, geometria, testo e indice di pagina dove l'entità è renderizzata, nonché la struttura complessiva e le relazioni. Utilizzare la combinazione di [GetEntity()](../) e [Current](./get_current/) per spostarsi all'entità che corrisponde a un nodo del documento. Per saperne di più, visita l'articolo di documentazione [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/).

```cpp
class LayoutEnumerator : public System::Object,
                         public System::Details::EnumeratorBasedIterator<System::SharedPtr<System::Object>>,
                         private System::Details::IteratorPointerUpdater<System::SharedPtr<System::Object>, false>
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [CloneIterator](./cloneiterator/)() const override |  |
| [get_Current](./get_current/)() const | Ottiene o imposta la posizione corrente nel modello di layout di pagina. Questa proprietà restituisce un oggetto opaco che corrisponde all'entità di layout corrente. |
| [get_Document](./get_document/)() const | Ottiene il documento che questa istanza enumera. |
| [get_Kind](./get_kind/)() | Restituisce il tipo dell'entità corrente. Può essere una stringa vuota ma mai **null**. |
| [get_PageIndex](./get_pageindex/)() | Restituisce l'indice basato su 1 di una pagina che contiene l'entità corrente. |
| [get_Rectangle](./get_rectangle/)() | Restituisce il rettangolo di delimitazione dell'entità corrente relativo all'angolo in alto a sinistra della pagina (in punti). |
| [get_Text](./get_text/)() | Restituisce il testo dell'entità span corrente. Genera eccezione per altri tipi di entità. |
| [get_Type](./get_type/)() | Restituisce il tipo dell'entità corrente. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | Restituisce una proprietà denominata dell'entità. |
| [IncrementIterator](./incrementiterator/)() override |  |
| [InitializeIterator](./initializeiterator/)() override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LayoutEnumerator](./layoutenumerator/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | Inizializza una nuova istanza di questa classe. |
| [MoveFirstChild](./movefirstchild/)() | Si sposta sulla prima entità figlio. |
| [MoveLastChild](./movelastchild/)() | Si sposta sull'ultima entità figlio. |
| [MoveNext](./movenext/)() | Si sposta sull'entità fratello successiva in ordine visivo. Quando si iterano le linee di un paragrafo interrotto tra pagine, questo metodo non si sposterà alla pagina successiva ma piuttosto all'entità successiva nella stessa pagina. |
| [MoveNextLogical](./movenextlogical/)() | Si sposta sull'entità fratello successiva in ordine logico. Quando si iterano le linee di un paragrafo interrotto tra pagine, questo metodo si sposterà alla linea successiva anche se si trova su un'altra pagina. |
| [MoveParent](./moveparent/)() | Si sposta sull'entità padre. |
| [MoveParent](./moveparent/)(Aspose::Words::Layout::LayoutEntityType) | Si sposta sull'entità padre del tipo specificato. |
| [MovePrevious](./moveprevious/)() | Si sposta sull'entità fratello precedente. |
| [MovePreviousLogical](./movepreviouslogical/)() | Si sposta sull'entità fratello precedente in ordine logico. Quando si iterano le linee di un paragrafo interrotto tra pagine, questo metodo si sposterà alla linea precedente anche se si trova su un'altra pagina. |
| [Reset](./reset/)() | Sposta l'enumeratore alla prima pagina del documento. |
| [set_Current](./set_current/)(const System::SharedPtr\<System::Object\>\&) | Setter per [Aspose::Words::Layout::LayoutEnumerator::get_Current](./get_current/). |
| static [Type](./type/)() |  |
## Vedi anche

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
