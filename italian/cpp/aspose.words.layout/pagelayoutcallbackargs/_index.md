---
title: "Aspose::Words::Layout::PageLayoutCallbackArgs class"
linktitle: "PageLayoutCallbackArgs"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Layout::PageLayoutCallbackArgs class. Un argomento passato a Notify(). Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.layout/pagelayoutcallbackargs/
---
## PageLayoutCallbackArgs class


Un argomento passato a [Notify()](../ipagelayoutcallback/notify/). Per saperne di più, visita l'articolo di documentazione [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/).

```cpp
class PageLayoutCallbackArgs : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_Document](./get_document/)() const | Ottiene il documento. |
| [get_Event](./get_event/)() const | Ottiene l'evento. |
| [get_PageIndex](./get_pageindex/)() | Ottiene l'indice basato su zero della pagina nel documento a cui si riferisce questo evento. Restituisce un valore negativo se non esiste una pagina associata, o se la pagina è stata rimossa durante il reflow. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Vedi anche

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
