---
title: "Método Aspose::Words::Drawing::AdjustmentCollection::idx_get"
linktitle: "idx_get"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Drawing::AdjustmentCollection::idx_get. Devuelve un ajuste en el índice especificado en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.drawing/adjustmentcollection/idx_get/
---
## AdjustmentCollection::idx_get method


Devuelve un ajuste en el índice especificado.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Adjustment> Aspose::Words::Drawing::AdjustmentCollection::idx_get(int32_t index)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| index | int32_t | Un índice en la colección. |

## Ejemplos



Muestra cómo trabajar con valores sin procesar de ajuste.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rounded rectangle shape.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

System::SharedPtr<Aspose::Words::Drawing::AdjustmentCollection> adjustments = shape->get_Adjustments();
ASSERT_EQ(1, adjustments->get_Count());

System::SharedPtr<Aspose::Words::Drawing::Adjustment> adjustment = adjustments->idx_get(0);
ASSERT_EQ(u"adj", adjustment->get_Name());
ASSERT_EQ(16667, adjustment->get_Value());

adjustment->set_Value(30000);

doc->Save(get_ArtifactsDir() + u"Shape.Adjustments.docx");
```

## Ver también

* Class [Adjustment](../../adjustment/)
* Class [AdjustmentCollection](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
