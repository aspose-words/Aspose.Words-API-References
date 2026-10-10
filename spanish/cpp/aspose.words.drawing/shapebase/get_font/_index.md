---
title: "Método Aspose::Words::Drawing::ShapeBase::get_Font"
linktitle: "get_Font"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Drawing::ShapeBase::get_Font. Proporciona acceso al formato de fuente de este objeto en C++."
type: docs
weight: 21000
url: /es/cpp/aspose.words.drawing/shapebase/get_font/
---
## ShapeBase::get_Font method


Proporciona acceso al formato de fuente de este objeto.

```cpp
System::SharedPtr<Aspose::Words::Font> Aspose::Words::Drawing::ShapeBase::get_Font()
```


## Ejemplos



Muestra cómo insertar un cuadro de texto y establecer la fuente de su contenido.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 300, 50);
builder->MoveTo(shape->get_LastParagraph());
builder->Write(u"This text is inside the text box.");

// Establezca la propiedad "Hidden" del objeto "Font" de la forma a "true" para ocultar el cuadro de texto de la vista
// y colapse el espacio que normalmente ocuparía.
// Establezca la propiedad "Hidden" del objeto "Font" de la forma a "false" para dejar el cuadro de texto visible.
shape->get_Font()->set_Hidden(hideShape);

// Si la forma es visible, modificaremos su apariencia mediante el objeto de fuente.
if (!hideShape)
{
    shape->get_Font()->set_HighlightColor(System::Drawing::Color::get_LightGray());
    shape->get_Font()->set_Color(System::Drawing::Color::get_Red());
    shape->get_Font()->set_Underline(Aspose::Words::Underline::Dash);
}

// Mueva el generador fuera del cuadro de texto de regreso al documento principal.
builder->MoveTo(shape->get_ParentParagraph());

builder->Writeln(u"\nThis text is outside the text box.");

doc->Save(get_ArtifactsDir() + u"Shape.Font.docx");
```

## Ver también

* Class [Font](../../../aspose.words/font/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
