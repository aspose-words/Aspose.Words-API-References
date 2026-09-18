---
title: "Aspose::Words::TabStopCollection::GetPositionByIndex method"
linktitle: "GetPositionByIndex"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::TabStopCollection::GetPositionByIndex Methode. Gibt die Position (in Punkten) des Tabstopps am angegebenen Index in C++ zurück."
type: docs
weight: 10000
url: /de/cpp/aspose.words/tabstopcollection/getpositionbyindex/
---
## TabStopCollection::GetPositionByIndex method


Gibt die Position (in Punkten) des Tabulators am angegebenen Index zurück.

```cpp
double Aspose::Words::TabStopCollection::GetPositionByIndex(int32_t index)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| index | int32_t | Ein Index in die Sammlung der Tabstopps. |

### ReturnValue

Die Position des Tabstopps.

## Beispiele



Zeigt, wie ein Tabstopp anhand seines Index gefunden und seine Position überprüft wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::TabStopCollection> tabStops = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat()->get_TabStops();

tabStops->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(30), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
tabStops->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(60), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);

// Überprüfe die Position des zweiten Tabstopps in der Sammlung.
ASSERT_NEAR(Aspose::Words::ConvertUtil::MillimeterToPoint(60), tabStops->GetPositionByIndex(1), 0.1);
```

## Siehe auch

* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
