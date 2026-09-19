---
title: "Metodo Aspose::Words::Drawing::Shape::get_Adjustments"
linktitle: "get_Adjustments"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Drawing::Shape::get_Adjustments. Fornisce l'accesso ai valori grezzi di regolazione di una forma. Per una forma che non contiene alcun valore grezzo di regolazione, restituisce una collezione vuota in C++."
type: docs
weight: 3834
url: /it/cpp/aspose.words.drawing/shape/get_adjustments/
---
## Shape::get_Adjustments method


Fornisce l'accesso ai valori grezzi di regolazione di una forma. Per una forma che non contiene alcun valore grezzo di regolazione, restituisce una collezione vuota.

```cpp
System::SharedPtr<Aspose::Words::Drawing::AdjustmentCollection> Aspose::Words::Drawing::Shape::get_Adjustments()
```


## Esempi



Mostra come lavorare con i valori grezzi di regolazione.
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

## Vedi anche

* Class [AdjustmentCollection](../../adjustmentcollection/)
* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
