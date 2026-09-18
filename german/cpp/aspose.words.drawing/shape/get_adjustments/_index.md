---
title: "Aspose::Words::Drawing::Shape::get_Adjustments-Methode"
linktitle: "get_Adjustments"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Shape::get_Adjustments-Methode. Stellt Zugriff auf die Rohwerte der Anpassungen einer Form bereit. Für eine Form, die keine Anpassungsrohwerte enthält, wird in C++ eine leere Sammlung zurückgegeben."
type: docs
weight: 3834
url: /de/cpp/aspose.words.drawing/shape/get_adjustments/
---
## Shape::get_Adjustments method


Stellt Zugriff auf die Rohwerte der Anpassungen einer Form bereit. Für eine Form, die keine Rohwerte für Anpassungen enthält, wird eine leere Sammlung zurückgegeben.

```cpp
System::SharedPtr<Aspose::Words::Drawing::AdjustmentCollection> Aspose::Words::Drawing::Shape::get_Adjustments()
```


## Beispiele



Zeigt, wie mit rohen Anpassungswerten gearbeitet wird.
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

## Siehe auch

* Class [AdjustmentCollection](../../adjustmentcollection/)
* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
