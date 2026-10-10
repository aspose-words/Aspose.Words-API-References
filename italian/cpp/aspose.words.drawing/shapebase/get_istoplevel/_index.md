---
title: "Aspose::Words::Drawing::ShapeBase::get_IsTopLevel metodo"
linktitle: "get_IsTopLevel"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::ShapeBase::get_IsTopLevel metodo. Restituisce true se questo shape non è un figlio di un group shape in C++."
type: docs
weight: 36000
url: /it/cpp/aspose.words.drawing/shapebase/get_istoplevel/
---
## ShapeBase::get_IsTopLevel method


Restituisce **true** se questa forma non è un figlio di una forma di gruppo.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsTopLevel()
```


## Esempi



Mostra come determinare se uno shape è parte di un group shape.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(200);
shape->set_Height(200);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

// Uno shape, per impostazione predefinita, non fa parte di alcun group shape e quindi ha la proprietà "IsTopLevel" impostata su "true".
ASSERT_TRUE(shape->get_IsTopLevel());

auto group = System::MakeObject<Aspose::Words::Drawing::GroupShape>(doc);
group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

// Una volta che assimiliamo uno shape in un group shape, la proprietà "IsTopLevel" cambia in "false".
ASSERT_FALSE(shape->get_IsTopLevel());
```

## Vedi anche

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
