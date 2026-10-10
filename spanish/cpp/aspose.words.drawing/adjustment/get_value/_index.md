---
title: "Aspose::Words::Drawing::Adjustment::get_Value método"
linktitle: "get_Value"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::Adjustment::get_Value método. Obtiene o establece el valor bruto del ajuste en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.drawing/adjustment/get_value/
---
## Adjustment::get_Value method


Obtiene o establece el valor bruto del ajuste.

```cpp
int32_t Aspose::Words::Drawing::Adjustment::get_Value() const
```


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

* Class [Adjustment](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
