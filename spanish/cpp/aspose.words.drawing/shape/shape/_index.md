---
title: "Aspose::Words::Drawing::Shape::Shape constructor"
linktitle: "Shape"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::Shape::Shape constructor. Crea un nuevo objeto shape en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.drawing/shape/shape/
---
## Shape::Shape constructor


Crea un nuevo objeto de forma.

```cpp
Aspose::Words::Drawing::Shape::Shape(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, Aspose::Words::Drawing::ShapeType shapeType)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | El documento propietario. |
| shapeType | Aspose::Words::Drawing::ShapeType | El tipo de la forma a crear. |
## Observaciones


Debe especificar las propiedades deseadas de la forma después de crearla.

## Ejemplos



Muestra cómo insertar una forma con una imagen del sistema de archivos local en un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// El constructor público de la clase "Shape" creará una forma con el tipo de marcado "ShapeMarkupLanguage.Vml".
// Si necesita crear una forma de un tipo no primitivo, como SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, o DiagonalCornersRounded,
// Por favor use DocumentBuilder.InsertShape.
auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Image);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Windows MetaFile.wmf");
shape->set_Width(100);
shape->set_Height(100);

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

doc->Save(get_ArtifactsDir() + u"Image.FromFile.docx");
```


Muestra cómo crear y formatear un cuadro de texto.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Crea un cuadro de texto flotante.
auto textBox = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::TextBox);
textBox->set_WrapType(Aspose::Words::Drawing::WrapType::None);
textBox->set_Height(50);
textBox->set_Width(200);

// Establece la alineación horizontal y vertical del texto dentro de la forma.
textBox->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
textBox->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Top);

// Agrega un párrafo al cuadro de texto y añade una secuencia de texto que el cuadro de texto mostrará.
textBox->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc));
System::SharedPtr<Aspose::Words::Paragraph> para = textBox->get_FirstParagraph();
para->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"Hello world!");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(textBox);

doc->Save(get_ArtifactsDir() + u"Shape.CreateTextBox.docx");
```

## Ver también

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Enum [ShapeType](../../shapetype/)
* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
