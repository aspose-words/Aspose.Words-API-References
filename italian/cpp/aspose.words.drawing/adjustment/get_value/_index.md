---
title: "Aspose::Words::Drawing::Adjustment::get_Value metodo"
linktitle: "get_Value"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Adjustment::get_Value metodo. Ottiene o imposta il valore grezzo della regolazione in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.drawing/adjustment/get_value/
---
## Adjustment::get_Value method


Ottiene o imposta il valore grezzo dell'aggiustamento.

```cpp
int32_t Aspose::Words::Drawing::Adjustment::get_Value() const
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

* Class [Adjustment](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
