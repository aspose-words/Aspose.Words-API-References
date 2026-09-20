---
title: "Método Aspose::Words::TabStopCollection::GetPositionByIndex"
linktitle: "GetPositionByIndex"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::TabStopCollection::GetPositionByIndex method. Obtiene la posición (en puntos) del tabulador en el índice especificado en C++."
type: docs
weight: 10000
url: /es/cpp/aspose.words/tabstopcollection/getpositionbyindex/
---
## TabStopCollection::GetPositionByIndex method


Obtiene la posición (en puntos) de la tabulación en el índice especificado.

```cpp
double Aspose::Words::TabStopCollection::GetPositionByIndex(int32_t index)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| index | int32_t | Un índice en la colección de tabuladores. |

### ReturnValue

La posición del tabulador.

## Ejemplos



Muestra cómo encontrar un tabulador por su índice y verificar su posición.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::TabStopCollection> tabStops = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat()->get_TabStops();

tabStops->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(30), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
tabStops->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(60), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);

// Verifique la posición del segundo tabulador en la colección.
ASSERT_NEAR(Aspose::Words::ConvertUtil::MillimeterToPoint(60), tabStops->GetPositionByIndex(1), 0.1);
```

## Ver también

* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
