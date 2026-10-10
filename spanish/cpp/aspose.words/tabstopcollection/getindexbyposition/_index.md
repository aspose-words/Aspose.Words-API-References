---
title: "Aspose::Words::TabStopCollection::GetIndexByPosition method"
linktitle: "GetIndexByPosition"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::TabStopCollection::GetIndexByPosition method. Obtiene el índice de un tabulador con la posición especificada en puntos en C++."
type: docs
weight: 9000
url: /es/cpp/aspose.words/tabstopcollection/getindexbyposition/
---
## TabStopCollection::GetIndexByPosition method


Obtiene el índice de una tabulación con la posición especificada en puntos.

```cpp
int32_t Aspose::Words::TabStopCollection::GetIndexByPosition(double position)
```


## Ejemplos



Muestra cómo buscar una posición para ver si existe un tabulador allí y obtener su índice.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::TabStopCollection> tabStops = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat()->get_TabStops();

// Agregue un tabulador en una posición de 30 mm.
tabStops->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(30), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);

// Un resultado de "0" devuelto por "GetIndexByPosition" confirma que un tabulador
// en 30 mm existe en esta colección, y está en el índice 0.
ASSERT_EQ(0, tabStops->GetIndexByPosition(Aspose::Words::ConvertUtil::MillimeterToPoint(30)));

// Un "-1" devuelto por "GetIndexByPosition" confirma que
// no hay ningún tabulador en esta colección con una posición de 60 mm.
ASSERT_EQ(-1, tabStops->GetIndexByPosition(Aspose::Words::ConvertUtil::MillimeterToPoint(60)));
```

## Ver también

* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
