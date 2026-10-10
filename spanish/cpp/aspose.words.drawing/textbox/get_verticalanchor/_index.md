---
title: "Aspose::Words::Drawing::TextBox::get_VerticalAnchor método"
linktitle: "get_VerticalAnchor"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::TextBox::get_VerticalAnchor método. Especifica la alineación vertical del texto dentro de una forma en C++."
type: docs
weight: 14000
url: /es/cpp/aspose.words.drawing/textbox/get_verticalanchor/
---
## TextBox::get_VerticalAnchor method


Especifica la alineación vertical del texto dentro de una forma.

```cpp
Aspose::Words::Drawing::TextBoxAnchor Aspose::Words::Drawing::TextBox::get_VerticalAnchor()
```

## Observaciones


El valor predeterminado es [Top](../../textboxanchor/).

## Ejemplos



Muestra cómo alinear verticalmente el contenido de texto de un cuadro de texto.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 200, 200);

// Establezca la propiedad "VerticalAnchor" a "TextBoxAnchor.Top" para
// alinear el texto en este cuadro de texto con el lado superior de la forma.
// Establezca la propiedad "VerticalAnchor" a "TextBoxAnchor.Middle" para
// alinear el texto en este cuadro de texto al centro de la forma.
// Establezca la propiedad "VerticalAnchor" a "TextBoxAnchor.Bottom" para
// alinear el texto en este cuadro de texto a la parte inferior de la forma.
shape->get_TextBox()->set_VerticalAnchor(verticalAnchor);

builder->MoveTo(shape->get_FirstParagraph());
builder->Write(u"Hello world!");

// La alineación vertical del texto dentro de los cuadros de texto está disponible a partir de Microsoft Word 2007.
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2007);
doc->Save(get_ArtifactsDir() + u"Shape.VerticalAnchor.docx");
```

## Ver también

* Enum [TextBoxAnchor](../../textboxanchor/)
* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
