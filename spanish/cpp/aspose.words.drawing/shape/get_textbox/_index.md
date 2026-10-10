---
title: "Método Aspose::Words::Drawing::Shape::get_TextBox"
linktitle: "get_TextBox"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Drawing::Shape::get_TextBox. Define atributos que especifican cómo se muestra el texto en una forma en C++."
type: docs
weight: 24000
url: /es/cpp/aspose.words.drawing/shape/get_textbox/
---
## Shape::get_TextBox method


Define atributos que especifican cómo se muestra el texto en una forma.

```cpp
System::SharedPtr<Aspose::Words::Drawing::TextBox> Aspose::Words::Drawing::Shape::get_TextBox()
```


## Ejemplos



Muestra cómo establecer la orientación del texto dentro de un cuadro de texto.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 150, 100);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();

// Mueve el generador de documentos al interior del TextBox y agrega texto.
builder->MoveTo(textBoxShape->get_LastParagraph());
builder->Writeln(u"Hello world!");
builder->Write(u"Hello again!");

// Establece la propiedad "LayoutFlow" para definir una orientación del contenido de texto de este cuadro de texto.
textBox->set_LayoutFlow(layoutFlow);

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxLayoutFlow.docx");
```

## Ver también

* Class [TextBox](../../textbox/)
* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
