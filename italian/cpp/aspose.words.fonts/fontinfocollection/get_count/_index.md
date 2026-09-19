---
title: "Metodo Aspose::Words::Fonts::FontInfoCollection::get_Count"
linktitle: "get_Count"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Fonts::FontInfoCollection::get_Count. Restituisce il numero di elementi contenuti nella collezione in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words.fonts/fontinfocollection/get_count/
---
## FontInfoCollection::get_Count method


Ottiene il numero di elementi contenuti nella raccolta.

```cpp
int32_t Aspose::Words::Fonts::FontInfoCollection::get_Count()
```


## Esempi



Mostra informazioni sui font presenti nel documento vuoto.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Un documento vuoto contiene 3 font predefiniti. Ogni font nel documento
// avrà un oggetto FontInfo corrispondente che contiene i dettagli di quel font.
ASSERT_EQ(3, doc->get_FontInfos()->get_Count());

ASSERT_TRUE(doc->get_FontInfos()->Contains(u"Times New Roman"));
ASSERT_EQ(204, doc->get_FontInfos()->idx_get(u"Times New Roman")->get_Charset());

ASSERT_TRUE(doc->get_FontInfos()->Contains(u"Symbol"));
ASSERT_TRUE(doc->get_FontInfos()->Contains(u"Arial"));
```

## Vedi anche

* Class [FontInfoCollection](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
