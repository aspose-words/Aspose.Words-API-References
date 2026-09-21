---
title: "Aspose::Words::TabStopCollection::GetPositionByIndex metod"
linktitle: "GetPositionByIndex"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::TabStopCollection::GetPositionByIndex metod. Hämtar positionen (i punkter) för tabbstoppet på det angivna indexet i C++."
type: docs
weight: 10000
url: /sv/cpp/aspose.words/tabstopcollection/getpositionbyindex/
---
## TabStopCollection::GetPositionByIndex method


Hämtar positionen (i punkter) för tabbstoppet på det angivna indexet.

```cpp
double Aspose::Words::TabStopCollection::GetPositionByIndex(int32_t index)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| index | int32_t | Ett index i samlingen av tabbstopp. |

### ReturnValue

Positionen för tabbstoppet.

## Exempel



Visar hur man hittar ett tabbstopp med dess index och verifierar dess position.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::TabStopCollection> tabStops = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat()->get_TabStops();

tabStops->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(30), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
tabStops->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(60), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);

// Verifiera positionen för det andra tabbstoppet i samlingen.
ASSERT_NEAR(Aspose::Words::ConvertUtil::MillimeterToPoint(60), tabStops->GetPositionByIndex(1), 0.1);
```

## Se även

* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
