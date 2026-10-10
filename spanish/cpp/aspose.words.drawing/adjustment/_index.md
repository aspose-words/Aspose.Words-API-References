---
title: "Aspose::Words::Drawing::Adjustment class"
linktitle: "Adjustment"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::Adjustment class. Representa valores de ajuste que se aplican a la forma especificada en C++."
type: docs
weight: 334
url: /es/cpp/aspose.words.drawing/adjustment/
---
## Adjustment class


Representa los valores de ajuste que se aplican a la forma especificada.

```cpp
class Adjustment : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_Name](./get_name/)() const | Obtiene el nombre del ajuste. |
| [get_Value](./get_value/)() const | Obtiene o establece el valor bruto del ajuste. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Value](./set_value/)(int32_t) | Establecedor para [Aspose::Words::Drawing::Adjustment::get_Value](./get_value/). |
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
