---
title: "Clase Aspose::Words::Drawing::AdjustmentCollection"
linktitle: "AdjustmentCollection"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Drawing::AdjustmentCollection. Representa una colección de solo lectura de valores de ajuste Adjustment que se aplican a la forma especificada en C++."
type: docs
weight: 667
url: /es/cpp/aspose.words.drawing/adjustmentcollection/
---
## AdjustmentCollection class


Representa una colección de solo lectura de valores de ajuste [Adjustment](../adjustment/) que se aplican a la forma especificada.

```cpp
class AdjustmentCollection : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_Count](./get_count/)() | Obtiene el número de elementos contenidos en la colección. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Devuelve un ajuste en el índice especificado. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
