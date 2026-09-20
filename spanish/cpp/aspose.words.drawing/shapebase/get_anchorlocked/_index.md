---
title: "Aspose::Words::Drawing::ShapeBase::get_AnchorLocked método"
linktitle: "get_AnchorLocked"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::ShapeBase::get_AnchorLocked método. Especifica si el ancla de la forma está bloqueada en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.drawing/shapebase/get_anchorlocked/
---
## ShapeBase::get_AnchorLocked method


Especifica si el ancla de la forma está bloqueada.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_AnchorLocked()
```

## Observaciones


El valor predeterminado es **false**.

Tiene efecto solo para formas de nivel superior.

Esta propiedad afecta el comportamiento del ancla de la forma en Microsoft Word. Cuando el ancla no está bloqueada, mover la forma en Microsoft Word puede mover también el ancla de la forma.

## Ejemplos



Muestra cómo bloquear o desbloquear el ancla de párrafo de una forma.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");

builder->Write(u"Our shape will have an anchor attached to this paragraph.");
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 200, 160);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);

builder->Writeln(u"Hello again!");

// Establezca la propiedad "AnchorLocked" en "true" para evitar el ancla de la forma
// de moverse al mover la forma en Microsoft Word.
// Establezca la propiedad "AnchorLocked" en "false" para permitir cualquier movimiento de la forma
// para también mover su ancla a cualquier otro párrafo al que la forma quede cerca.
shape->set_AnchorLocked(anchorLocked);

// Si la forma no tiene un símbolo de anclaje visible a su izquierda,
// necesitaremos habilitar los anclajes visibles a través de "Options" -> "Display" -> "Object Anchors".
doc->Save(get_ArtifactsDir() + u"Shape.AnchorLocked.docx");
```

## Ver también

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
