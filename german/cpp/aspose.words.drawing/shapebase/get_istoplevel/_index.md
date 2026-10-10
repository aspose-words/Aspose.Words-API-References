---
title: "Aspose::Words::Drawing::ShapeBase::get_IsTopLevel Methode"
linktitle: "get_IsTopLevel"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ShapeBase::get_IsTopLevel Methode. Gibt true zurück, wenn diese Form kein Kind einer Gruppenform ist in C++."
type: docs
weight: 36000
url: /de/cpp/aspose.words.drawing/shapebase/get_istoplevel/
---
## ShapeBase::get_IsTopLevel method


Gibt **true** zurück, wenn diese Form kein Kind einer Gruppenform ist.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsTopLevel()
```


## Beispiele



Zeigt, wie man erkennt, ob eine Form Teil einer Gruppenform ist.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(200);
shape->set_Height(200);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

// Eine Form ist standardmäßig nicht Teil einer Gruppenform und hat daher die Eigenschaft "IsTopLevel" auf "true" gesetzt.
ASSERT_TRUE(shape->get_IsTopLevel());

auto group = System::MakeObject<Aspose::Words::Drawing::GroupShape>(doc);
group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

// Sobald wir eine Form in eine Gruppenform integrieren, ändert sich die Eigenschaft "IsTopLevel" zu "false".
ASSERT_FALSE(shape->get_IsTopLevel());
```

## Siehe auch

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
