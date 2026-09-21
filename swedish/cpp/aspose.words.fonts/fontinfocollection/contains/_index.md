---
title: "Aspose::Words::Fonts::FontInfoCollection::Contains metod"
linktitle: "Contains"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fonts::FontInfoCollection::Contains metod. Avgör om samlingen innehåller ett teckensnitt med det angivna namnet i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words.fonts/fontinfocollection/contains/
---
## FontInfoCollection::Contains method


Bestämmer om samlingen innehåller ett teckensnitt med det angivna namnet.

```cpp
bool Aspose::Words::Fonts::FontInfoCollection::Contains(const System::String &name)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| namn | const System::String\& | Skiftlägesokänsligt namn på teckensnittet att hitta. |

### ReturnValue

**true** if the item is found in the collection; otherwise, **false**.

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
