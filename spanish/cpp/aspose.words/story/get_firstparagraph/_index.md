---
title: "Aspose::Words::Story::get_FirstParagraph método"
linktitle: "get_FirstParagraph"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Story::get_FirstParagraph método. Obtiene el primer párrafo de la historia en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words/story/get_firstparagraph/
---
## Story::get_FirstParagraph method


Obtiene el primer párrafo de la historia.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::Story::get_FirstParagraph() override
```


## Ejemplos



Muestra cómo formatear una corrida de texto usando su propiedad de fuente.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");

System::SharedPtr<Aspose::Words::Font> font = run->get_Font();
font->set_Name(u"Courier New");
font->set_Size(36);
font->set_HighlightColor(System::Drawing::Color::get_Yellow());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);
doc->Save(get_ArtifactsDir() + u"Font.CreateFormattedRun.docx");
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

* Class [Paragraph](../../paragraph/)
* Class [Story](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
