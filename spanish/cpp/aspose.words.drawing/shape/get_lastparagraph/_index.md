---
title: "Método Aspose::Words::Drawing::Shape::get_LastParagraph"
linktitle: "get_LastParagraph"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Drawing::Shape::get_LastParagraph. Obtiene el último párrafo en la forma en C++."
type: docs
weight: 14000
url: /es/cpp/aspose.words.drawing/shape/get_lastparagraph/
---
## Shape::get_LastParagraph method


Obtiene el último párrafo en la forma.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::Drawing::Shape::get_LastParagraph()
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

* Class [Paragraph](../../../aspose.words/paragraph/)
* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
