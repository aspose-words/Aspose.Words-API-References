---
title: "Aspose::Words::TabStopCollection::GetIndexByPosition metod"
linktitle: "GetIndexByPosition"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::TabStopCollection::GetIndexByPosition metod. Hämtar indexet för ett tabbstopp med den angivna positionen i punkter i C++."
type: docs
weight: 9000
url: /sv/cpp/aspose.words/tabstopcollection/getindexbyposition/
---
## TabStopCollection::GetIndexByPosition method


Hämtar indexet för ett tabbstopp med den angivna positionen i punkter.

```cpp
int32_t Aspose::Words::TabStopCollection::GetIndexByPosition(double position)
```


## Exempel



Visar hur man söker upp en position för att se om ett tabbstopp finns där och erhålla dess index.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::TabStopCollection> tabStops = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat()->get_TabStops();

// Lägg till ett tabbstopp på positionen 30 mm.
tabStops->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(30), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);

// Ett resultat på "0" som returneras av "GetIndexByPosition" bekräftar att ett tabbstopp
// vid 30 mm finns i denna samling, och det är på index 0.
ASSERT_EQ(0, tabStops->GetIndexByPosition(Aspose::Words::ConvertUtil::MillimeterToPoint(30)));

// Ett "-1" som returneras av "GetIndexByPosition" bekräftar att
// det inte finns något tabbstopp i denna samling med positionen 60 mm.
ASSERT_EQ(-1, tabStops->GetIndexByPosition(Aspose::Words::ConvertUtil::MillimeterToPoint(60)));
```

## Se även

* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
