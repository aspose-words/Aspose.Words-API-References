---
title: "Aspose::Words::Drawing::Shape::Shape konstruktor"
linktitle: "Shape"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Shape::Shape konstruktor. Skapar ett nytt formobjekt i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.drawing/shape/shape/
---
## Shape::Shape constructor


Skapar ett nytt form‑objekt.

```cpp
Aspose::Words::Drawing::Shape::Shape(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, Aspose::Words::Drawing::ShapeType shapeType)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Ägandokumentet. |
| shapeType | Aspose::Words::Drawing::ShapeType | Typen av formen som ska skapas. |
## Anmärkningar


Du bör ange önskade formegenskaper efter att du har skapat en form.

## Exempel



Visar hur man infogar en form med en bild från det lokala filsystemet i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Den offentliga konstruktorn för klassen "Shape" skapar en form med markup-typen "ShapeMarkupLanguage.Vml".
// Om du behöver skapa en form av en icke-primitive typ, såsom SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, eller DiagonalCornersRounded,
// vänligen använd DocumentBuilder.InsertShape.
auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Image);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Windows MetaFile.wmf");
shape->set_Width(100);
shape->set_Height(100);

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

doc->Save(get_ArtifactsDir() + u"Image.FromFile.docx");
```


Visar hur man skapar och formaterar en textruta.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Skapa en flytande textruta.
auto textBox = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::TextBox);
textBox->set_WrapType(Aspose::Words::Drawing::WrapType::None);
textBox->set_Height(50);
textBox->set_Width(200);

// Ställ in horisontell och vertikal justering av texten i formen.
textBox->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
textBox->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Top);

// Lägg till ett stycke i textrutan och lägg till en körning av text som textrutan kommer att visa.
textBox->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc));
System::SharedPtr<Aspose::Words::Paragraph> para = textBox->get_FirstParagraph();
para->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"Hello world!");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(textBox);

doc->Save(get_ArtifactsDir() + u"Shape.CreateTextBox.docx");
```

## Se även

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Enum [ShapeType](../../shapetype/)
* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
