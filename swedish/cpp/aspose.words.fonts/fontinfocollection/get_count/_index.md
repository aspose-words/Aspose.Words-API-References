---
title: "Aspose::Words::Fonts::FontInfoCollection::get_Count‑metod"
linktitle: "get_Count"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fonts::FontInfoCollection::get_Count‑metod. Hämtar antalet element som finns i samlingen i C++."
type: docs
weight: 7000
url: /sv/cpp/aspose.words.fonts/fontinfocollection/get_count/
---
## FontInfoCollection::get_Count method


Hämtar antalet element som finns i samlingen.

```cpp
int32_t Aspose::Words::Fonts::FontInfoCollection::get_Count()
```


## Exempel



Visar information om de teckensnitt som finns i det tomma dokumentet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Ett tomt dokument innehåller 3 standardteckensnitt. Varje teckensnitt i dokumentet
// kommer att ha ett motsvarande FontInfo‑objekt som innehåller detaljer om det teckensnittet.
ASSERT_EQ(3, doc->get_FontInfos()->get_Count());

ASSERT_TRUE(doc->get_FontInfos()->Contains(u"Times New Roman"));
ASSERT_EQ(204, doc->get_FontInfos()->idx_get(u"Times New Roman")->get_Charset());

ASSERT_TRUE(doc->get_FontInfos()->Contains(u"Symbol"));
ASSERT_TRUE(doc->get_FontInfos()->Contains(u"Arial"));
```

## Se även

* Class [FontInfoCollection](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
