---
title: "Classe Aspose::Words::Drawing::AdjustmentCollection"
linktitle: "AdjustmentCollection"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::Drawing::AdjustmentCollection. Rappresenta una collezione di sola lettura di valori di regolazione Adjustment che vengono applicati alla forma specificata in C++."
type: docs
weight: 667
url: /it/cpp/aspose.words.drawing/adjustmentcollection/
---
## AdjustmentCollection class


Rappresenta una collezione di sola lettura di valori di regolazione [Adjustment](../adjustment/) che vengono applicati alla forma specificata.

```cpp
class AdjustmentCollection : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_Count](./get_count/)() | Ottiene il numero di elementi contenuti nella raccolta. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Restituisce una regolazione all'indice specificato. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
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
