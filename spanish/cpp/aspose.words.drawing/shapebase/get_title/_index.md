---
title: "Aspose::Words::Drawing::ShapeBase::get_Title método"
linktitle: "get_Title"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::ShapeBase::get_Title método. Obtiene o establece el título (leyenda) del objeto de forma actual en C++."
type: docs
weight: 51000
url: /es/cpp/aspose.words.drawing/shapebase/get_title/
---
## ShapeBase::get_Title method


Obtiene o establece el título (leyenda) del objeto de forma actual.

```cpp
System::String Aspose::Words::Drawing::ShapeBase::get_Title()
```

## Observaciones


El valor predeterminado es una cadena vacía.

No puede ser **null**, pero puede ser una cadena vacía.

## Ejemplos



Muestra cómo establecer el título de una forma.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Cree una forma, asígnele un título y luego agréguela al documento.
auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Cube);
shape->set_Width(200);
shape->set_Height(200);
shape->set_Title(u"My cube");

builder->InsertNode(shape);

// Cuando guardamos un documento con una forma que tiene un título,
// Aspose.Words almacenará ese título en el Alt Text de la forma.
doc->Save(get_ArtifactsDir() + u"Shape.Title.docx");

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.Title.docx");
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

ASSERT_EQ(System::String::Empty, shape->get_Title());
ASSERT_EQ(u"Title: My cube", shape->get_AlternativeText());
```

## Ver también

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
