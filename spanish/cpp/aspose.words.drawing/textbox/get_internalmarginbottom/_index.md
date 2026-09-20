---
title: "Método Aspose::Words::Drawing::TextBox::get_InternalMarginBottom"
linktitle: "get_InternalMarginBottom"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Drawing::TextBox::get_InternalMarginBottom. Especifica el margen interior inferior en puntos para una forma en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.drawing/textbox/get_internalmarginbottom/
---
## TextBox::get_InternalMarginBottom method


Especifica el margen interior inferior en puntos para una forma.

```cpp
double Aspose::Words::Drawing::TextBox::get_InternalMarginBottom()
```

## Observaciones


El valor predeterminado es 1/20 pulgada.

## Ejemplos



Muestra cómo establecer márgenes internos para un cuadro de texto.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserta otro cuadro de texto con márgenes específicos.
System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 100, 100);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();
textBox->set_InternalMarginTop(15);
textBox->set_InternalMarginBottom(15);
textBox->set_InternalMarginLeft(15);
textBox->set_InternalMarginRight(15);

builder->MoveTo(textBoxShape->get_LastParagraph());
builder->Write(u"Text placed according to textbox margins.");

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxMargins.docx");
```

## Ver también

* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
