---
title: "Método Aspose::Words::Story::get_StoryType"
linktitle: "get_StoryType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Story::get_StoryType método. Obtiene el tipo de esta historia en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words/story/get_storytype/
---
## Story::get_StoryType method


Obtiene el tipo de esta historia.

```cpp
Aspose::Words::StoryType Aspose::Words::Story::get_StoryType() override
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

* Enum [StoryType](../../storytype/)
* Class [Story](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
