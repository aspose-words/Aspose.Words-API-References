---
title: "Aspose::Words::Story::DeleteShapes método"
linktitle: "DeleteShapes"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Story::DeleteShapes método. Elimina todas las formas del texto de esta historia en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words/story/deleteshapes/
---
## Story::DeleteShapes method


Elimina todas las formas del texto de esta historia.

```cpp
void Aspose::Words::Story::DeleteShapes()
```


## Ejemplos



Muestra cómo eliminar todas las formas de un nodo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Use un DocumentBuilder para insertar una forma. Esta es una forma en línea,
// que tiene un Paragraph padre, que es un nodo hijo del Body de la primera sección.
builder->InsertShape(Aspose::Words::Drawing::ShapeType::Cube, 100.0, 100.0);

ASSERT_EQ(1, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());

// Podemos eliminar todas las formas de los párrafos hijos de este Body.
ASSERT_EQ(Aspose::Words::StoryType::MainText, doc->get_FirstSection()->get_Body()->get_StoryType());
doc->get_FirstSection()->get_Body()->DeleteShapes();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
```

## Ver también

* Class [Story](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
