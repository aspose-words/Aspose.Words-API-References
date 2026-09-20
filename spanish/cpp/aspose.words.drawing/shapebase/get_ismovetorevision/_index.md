---
title: "Método Aspose::Words::Drawing::ShapeBase::get_IsMoveToRevision"
linktitle: "get_IsMoveToRevision"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Drawing::ShapeBase::get_IsMoveToRevision. Devuelve true si este objeto fue movido (insertado) en Microsoft Word mientras el seguimiento de cambios estaba habilitado en C++."
type: docs
weight: 34000
url: /es/cpp/aspose.words.drawing/shapebase/get_ismovetorevision/
---
## ShapeBase::get_IsMoveToRevision method


Devuelve **true** si este objeto fue movido (insertado) en Microsoft Word mientras el seguimiento de cambios estaba habilitado.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsMoveToRevision()
```


## Ejemplos



Muestra cómo identificar formas de revisión de movimiento.
```cpp
// Una revisión de movimiento es cuando movemos un elemento en el cuerpo del documento mediante cortar y pegar en Microsoft Word mientras
// seguimiento de cambios. Si involucramos una forma en línea en dicho movimiento de texto, esa forma también será una revisión.
// Copiar y pegar o mover formas flotantes no crean revisiones de movimiento.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revision shape.docx");

// Las revisiones de movimiento consisten en pares de "Move from" y "Move to". Movimos en este documento una forma,
// pero hasta que aceptemos o rechacemos la revisión de movimiento, habrá dos instancias de esa forma.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(2, shapes->get_Length());

// Esta es la revisión "Move to", que es la forma en su destino de llegada.
// Si aceptamos la revisión, esta forma de revisión "Move to" desaparecerá,
// y la forma de revisión "Move from" permanecerá.
ASSERT_FALSE(shapes[0]->get_IsMoveFromRevision());
ASSERT_TRUE(shapes[0]->get_IsMoveToRevision());

// Esta es la revisión "Move from", que es la forma en su ubicación original.
// Si aceptamos la revisión, esta forma de revisión "Move from" desaparecerá,
// y la forma de revisión "Move to" permanecerá.
ASSERT_TRUE(shapes[1]->get_IsMoveFromRevision());
ASSERT_FALSE(shapes[1]->get_IsMoveToRevision());
```

## Ver también

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
