---
title: "Aspose::Words::Drawing::ShapeBase::get_IsTopLevel método"
linktitle: "get_IsTopLevel"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::ShapeBase::get_IsTopLevel método. Devuelve true si esta forma no es un hijo de una forma de grupo en C++."
type: docs
weight: 36000
url: /es/cpp/aspose.words.drawing/shapebase/get_istoplevel/
---
## ShapeBase::get_IsTopLevel method


Devuelve **true** si esta forma no es un hijo de una forma de grupo.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsTopLevel()
```


## Ejemplos



Muestra cómo determinar si una forma es parte de una forma de grupo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(200);
shape->set_Height(200);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

// Una forma, por defecto, no forma parte de ninguna forma de grupo, y por lo tanto tiene la propiedad "IsTopLevel" establecida en "true".
ASSERT_TRUE(shape->get_IsTopLevel());

auto group = System::MakeObject<Aspose::Words::Drawing::GroupShape>(doc);
group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

// Una vez que incorporamos una forma a una forma de grupo, la propiedad "IsTopLevel" cambia a "false".
ASSERT_FALSE(shape->get_IsTopLevel());
```

## Ver también

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
