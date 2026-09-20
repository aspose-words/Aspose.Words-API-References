---
title: "Aspose::Words::Drawing::TextBoxAnchor enum"
linktitle: "TextBoxAnchor"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::TextBoxAnchor enum. Especifica los valores usados para la alineación vertical del texto de la forma en C++."
type: docs
weight: 39000
url: /es/cpp/aspose.words.drawing/textboxanchor/
---
## TextBoxAnchor enum


Especifica los valores usados para la alineación vertical del texto de la forma.

```cpp
enum class TextBoxAnchor
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Superior | 0 | El texto está alineado a la parte superior del cuadro de texto. |
| Medio | 1 | El texto está alineado al medio del cuadro de texto. |
| Inferior | 2 | El texto está alineado a la parte inferior del cuadro de texto. |
| TopCentered | 3 | El texto está alineado al centro superior del cuadro de texto. |
| MiddleCentered | 4 | El texto está alineado al centro medio del cuadro de texto. |
| BottomCentered | 5 | El texto está alineado al centro inferior del cuadro de texto. |
| TopBaseline | 6 | El texto está alineado a la línea base superior del cuadro de texto. |
| BottomBaseline | 7 | El texto está alineado a la línea base inferior del cuadro de texto. |
| TopCenteredBaseline | 8 | El texto está alineado a la línea base centrada superior del cuadro de texto. |
| BottomCenteredBaseline | 9 | El texto está alineado a la línea base centrada inferior del cuadro de texto. |


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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
