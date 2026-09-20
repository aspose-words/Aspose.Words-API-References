---
title: "Aspose::Words::Drawing::TextBoxWrapMode enum"
linktitle: "TextBoxWrapMode"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::TextBoxWrapMode enum. Especifica cómo se ajusta el texto dentro de una forma en C++."
type: docs
weight: 40000
url: /es/cpp/aspose.words.drawing/textboxwrapmode/
---
## TextBoxWrapMode enum


Especifica cómo se ajusta el texto dentro de una forma.

```cpp
enum class TextBoxWrapMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Square | 0 | El texto se ajusta dentro de una forma. |
| None | 2 | El texto no se ajusta dentro de una forma. |


## Ejemplos



Muestra cómo establecer un modo de ajuste para el contenido de un cuadro de texto.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 300, 300);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();

// Establezca la propiedad "TextBoxWrapMode" a "TextBoxWrapMode.None" para aumentar el ancho del cuadro de texto
// para acomodar el texto, debería ser lo suficientemente grande.
// Establezca la propiedad "TextBoxWrapMode" a "TextBoxWrapMode.Square" para
// ajustar todo el texto dentro del cuadro de texto, preservando sus dimensiones.
textBox->set_TextBoxWrapMode(textBoxWrapMode);

builder->MoveTo(textBoxShape->get_LastParagraph());
builder->get_Font()->set_Size(32);
builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxContentsWrapMode.docx");
```

## Ver también

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
