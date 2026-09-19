---
title: "Metodo Aspose::Words::TabStopCollection::GetPositionByIndex"
linktitle: "GetPositionByIndex"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::TabStopCollection::GetPositionByIndex method. Ottiene la posizione (in punti) della tabulazione all'indice specificato in C++."
type: docs
weight: 10000
url: /it/cpp/aspose.words/tabstopcollection/getpositionbyindex/
---
## TabStopCollection::GetPositionByIndex method


Restituisce la posizione (in punti) della tabulazione all'indice specificato.

```cpp
double Aspose::Words::TabStopCollection::GetPositionByIndex(int32_t index)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| index | int32_t | Un indice nella raccolta di tabulazioni. |

### ReturnValue

La posizione della tabulazione.

## Esempi



Mostra come trovare una tabulazione per indice e verificare la sua posizione.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::TabStopCollection> tabStops = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat()->get_TabStops();

tabStops->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(30), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
tabStops->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(60), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);

// Verifica la posizione della seconda tabulazione nella raccolta.
ASSERT_NEAR(Aspose::Words::ConvertUtil::MillimeterToPoint(60), tabStops->GetPositionByIndex(1), 0.1);
```

## Vedi anche

* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
