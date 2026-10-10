---
title: "Aspose::Words::Drawing::ShapeBase::get_IsInsertRevision método"
linktitle: "get_IsInsertRevision"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::ShapeBase::get_IsInsertRevision método. Devuelve true si este objeto fue insertado en Microsoft Word mientras el seguimiento de cambios estaba habilitado en C++."
type: docs
weight: 31000
url: /es/cpp/aspose.words.drawing/shapebase/get_isinsertrevision/
---
## ShapeBase::get_IsInsertRevision method


Devuelve true si este objeto fue insertado en Microsoft Word mientras el seguimiento de cambios estaba habilitado.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsInsertRevision()
```


## Ejemplos



Muestra cómo trabajar con formas de revisión.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_FALSE(doc->get_TrackRevisions());

// Inserte una forma en línea sin rastrear revisiones, lo que hará que esta forma no sea una revisión de ningún tipo.
auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Cube);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
shape->set_Width(100.0);
shape->set_Height(100.0);
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

// Comience a rastrear revisiones y luego inserte otra forma, lo que será una revisión.
doc->StartTrackRevisions(u"John Doe");

shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Sun);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
shape->set_Width(100.0);
shape->set_Height(100.0);
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(2, shapes->get_Length());

shapes[0]->Remove();

// Dado que eliminamos esa forma mientras estábamos rastreando cambios,
// la forma persiste en el documento y cuenta como una revisión de eliminación.
// Aceptar esta revisión eliminará la forma permanentemente, y rechazarla la mantendrá en el documento.
ASSERT_EQ(Aspose::Words::Drawing::ShapeType::Cube, shapes[0]->get_ShapeType());
ASSERT_TRUE(shapes[0]->get_IsDeleteRevision());

// Y insertamos otra forma mientras rastreábamos cambios, por lo que esa forma contará como una revisión de inserción.
// Aceptar esta revisión asimilará esta forma al documento como una no-revisión,
// y rechazar la revisión eliminará esta forma permanentemente.
ASSERT_EQ(Aspose::Words::Drawing::ShapeType::Sun, shapes[1]->get_ShapeType());
ASSERT_TRUE(shapes[1]->get_IsInsertRevision());
```

## Ver también

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
