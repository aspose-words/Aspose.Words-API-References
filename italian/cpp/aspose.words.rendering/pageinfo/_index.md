---
title: "Aspose::Words::Rendering::PageInfo classe"
linktitle: "PageInfo"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Rendering::PageInfo classe. Rappresenta le informazioni su una pagina specifica del documento. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.rendering/pageinfo/
---
## PageInfo class


Rappresenta le informazioni su una specifica pagina del documento. Per saperne di più, visita l'articolo di documentazione [Rendering](https://docs.aspose.com/words/cpp/rendering/).

```cpp
class PageInfo : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_Colored](./get_colored/)() | Restituisce **true** se la pagina contiene contenuto a colori. |
| [get_HeightInPoints](./get_heightinpoints/)() | Ottiene l'altezza della pagina in punti. |
| [get_Landscape](./get_landscape/)() const | Restituisce **true** se l'orientamento della pagina specificato nel documento per questa pagina è orizzontale. |
| [get_PaperSize](./get_papersize/)() | Ottiene la dimensione della carta come enumerazione. |
| [get_PaperTray](./get_papertray/)() const | Ottiene il vassoio della carta (bin) per questa pagina come specificato nel documento. Il valore è specifico dell'implementazione (stampante). |
| [get_SizeInPoints](./get_sizeinpoints/)() const | Ottiene la dimensione della pagina in punti. |
| [get_WidthInPoints](./get_widthinpoints/)() | Ottiene la larghezza della pagina in punti. |
| [GetSizeInPixels](./getsizeinpixels/)(float, float) | Calcola la dimensione della pagina in pixel per un fattore di zoom e una risoluzione specificati. |
| [GetSizeInPixels](./getsizeinpixels/)(float, float, float) | Calcola la dimensione della pagina in pixel per un fattore di zoom e una risoluzione specificati. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Note


La larghezza e l'altezza della pagina restituiti da questo oggetto rappresentano la dimensione "finale" della pagina, ad esempio sono già ruotati all'orientamento corretto.

## Vedi anche

* Namespace [Aspose::Words::Rendering](../)
* Library [Aspose.Words for C++](../../)
