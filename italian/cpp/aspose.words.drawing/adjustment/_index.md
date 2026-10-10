---
title: "Aspose::Words::Drawing::Adjustment class"
linktitle: "Adjustment"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Adjustment class. Rappresenta i valori di aggiustamento applicati alla forma specificata in C++."
type: docs
weight: 334
url: /it/cpp/aspose.words.drawing/adjustment/
---
## Adjustment class


Rappresenta i valori di regolazione applicati alla forma specificata.

```cpp
class Adjustment : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_Name](./get_name/)() const | Ottiene il nome dell'aggiustamento. |
| [get_Value](./get_value/)() const | Ottiene o imposta il valore grezzo dell'aggiustamento. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Value](./set_value/)(int32_t) | Setter per [Aspose::Words::Drawing::Adjustment::get_Value](./get_value/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
