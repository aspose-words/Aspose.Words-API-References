---
title: "Aspose::Words::Drawing::ShapeBase::get_IsTopLevel metod"
linktitle: "get_IsTopLevel"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ShapeBase::get_IsTopLevel metod. Returnerar true om denna form inte är ett barn till en gruppform i C++."
type: docs
weight: 36000
url: /sv/cpp/aspose.words.drawing/shapebase/get_istoplevel/
---
## ShapeBase::get_IsTopLevel method


Returnerar **true** om denna form inte är ett barn till en gruppform.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsTopLevel()
```


## Exempel



Visar hur man avgör om en form är en del av en gruppform.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(200);
shape->set_Height(200);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

// En form är som standard inte en del av någon gruppform, och har därför egenskapen "IsTopLevel" satt till "true".
ASSERT_TRUE(shape->get_IsTopLevel());

auto group = System::MakeObject<Aspose::Words::Drawing::GroupShape>(doc);
group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

// När vi integrerar en form i en gruppform ändras egenskapen "IsTopLevel" till "false".
ASSERT_FALSE(shape->get_IsTopLevel());
```

## Se även

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
