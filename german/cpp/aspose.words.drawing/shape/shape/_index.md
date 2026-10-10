---
title: "Aspose::Words::Drawing::Shape::Shape-Konstruktor"
linktitle: "Shape"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Shape::Shape-Konstruktor. Erstellt ein neues Form-Objekt in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.drawing/shape/shape/
---
## Shape::Shape constructor


Erstellt ein neues Form‑Objekt.

```cpp
Aspose::Words::Drawing::Shape::Shape(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, Aspose::Words::Drawing::ShapeType shapeType)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Das Eigentümerdokument. |
| shapeType | Aspose::Words::Drawing::ShapeType | Der Typ der zu erstellenden Form. |
## Hinweise


Sie sollten die gewünschten Shape-Eigenschaften angeben, nachdem Sie ein Shape erstellt haben.

## Beispiele



Zeigt, wie man eine Form mit einem Bild aus dem lokalen Dateisystem in ein Dokument einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Der öffentliche Konstruktor der "Shape"-Klasse erstellt eine Form mit dem Markup-Typ "ShapeMarkupLanguage.Vml".
// Wenn Sie eine Form eines nicht‑primitiven Typs erstellen müssen, wie SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded oder DiagonalCornersRounded,
// verwenden Sie bitte DocumentBuilder.InsertShape.
auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Image);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Windows MetaFile.wmf");
shape->set_Width(100);
shape->set_Height(100);

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

doc->Save(get_ArtifactsDir() + u"Image.FromFile.docx");
```


Zeigt, wie man ein Textfeld erstellt und formatiert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Erstelle ein schwebendes Textfeld.
auto textBox = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::TextBox);
textBox->set_WrapType(Aspose::Words::Drawing::WrapType::None);
textBox->set_Height(50);
textBox->set_Width(200);

// Lege die horizontale und vertikale Ausrichtung des Textes innerhalb der Form fest.
textBox->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
textBox->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Top);

// Füge dem Textfeld einen Absatz hinzu und füge einen Textlauf hinzu, den das Textfeld anzeigen soll.
textBox->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc));
System::SharedPtr<Aspose::Words::Paragraph> para = textBox->get_FirstParagraph();
para->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"Hello world!");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(textBox);

doc->Save(get_ArtifactsDir() + u"Shape.CreateTextBox.docx");
```

## Siehe auch

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Enum [ShapeType](../../shapetype/)
* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
