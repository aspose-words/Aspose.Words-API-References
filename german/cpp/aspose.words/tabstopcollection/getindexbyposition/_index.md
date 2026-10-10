---
title: "Aspose::Words::TabStopCollection::GetIndexByPosition-Methode"
linktitle: "GetIndexByPosition"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::TabStopCollection::GetIndexByPosition-Methode. Gibt den Index eines Tabstopps mit der angegebenen Position in Punkten in C++ zurück."
type: docs
weight: 9000
url: /de/cpp/aspose.words/tabstopcollection/getindexbyposition/
---
## TabStopCollection::GetIndexByPosition method


Gibt den Index eines Tabulators mit der angegebenen Position in Punkten zurück.

```cpp
int32_t Aspose::Words::TabStopCollection::GetIndexByPosition(double position)
```


## Beispiele



Zeigt, wie man eine Position nachschlägt, um zu prüfen, ob dort ein Tabstopp existiert, und dessen Index zu erhalten.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::TabStopCollection> tabStops = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat()->get_TabStops();

// Füge einen Tabstopp an einer Position von 30 mm hinzu.
tabStops->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(30), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);

// Ein Ergebnis von "0", das von "GetIndexByPosition" zurückgegeben wird, bestätigt, dass ein Tabstopp
// bei 30 mm in dieser Sammlung existiert, und er sich an Index 0 befindet.
ASSERT_EQ(0, tabStops->GetIndexByPosition(Aspose::Words::ConvertUtil::MillimeterToPoint(30)));

// Ein "-1", das von "GetIndexByPosition" zurückgegeben wird, bestätigt, dass
// in dieser Sammlung kein Tabstopp mit einer Position von 60 mm existiert.
ASSERT_EQ(-1, tabStops->GetIndexByPosition(Aspose::Words::ConvertUtil::MillimeterToPoint(60)));
```

## Siehe auch

* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
