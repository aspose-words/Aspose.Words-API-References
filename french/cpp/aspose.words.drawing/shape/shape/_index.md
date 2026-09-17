---
title: "Aspose::Words::Drawing::Shape::Shape constructeur"
linktitle: "Shape"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Shape::Shape constructeur. Crée un nouvel objet shape en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.drawing/shape/shape/
---
## Shape::Shape constructor


Crée un nouvel objet forme.

```cpp
Aspose::Words::Drawing::Shape::Shape(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, Aspose::Words::Drawing::ShapeType shapeType)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Le document propriétaire. |
| shapeType | Aspose::Words::Drawing::ShapeType | Le type de la forme à créer. |
## Remarques


Vous devez spécifier les propriétés de forme souhaitées après avoir créé une forme.

## Exemples



Montre comment insérer une forme avec une image depuis le système de fichiers local dans un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Le constructeur public de la classe "Shape" créera une forme avec le type de balisage "ShapeMarkupLanguage.Vml".
// Si vous devez créer une forme d'un type non primitif, tel que SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, ou DiagonalCornersRounded,
// veuillez utiliser DocumentBuilder.InsertShape.
auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Image);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Windows MetaFile.wmf");
shape->set_Width(100);
shape->set_Height(100);

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

doc->Save(get_ArtifactsDir() + u"Image.FromFile.docx");
```


Montre comment créer et formater une zone de texte.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Créez une zone de texte flottante.
auto textBox = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::TextBox);
textBox->set_WrapType(Aspose::Words::Drawing::WrapType::None);
textBox->set_Height(50);
textBox->set_Width(200);

// Définissez l’alignement horizontal et vertical du texte à l’intérieur de la forme.
textBox->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
textBox->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Top);

// Ajoutez un paragraphe à la zone de texte et ajoutez un segment de texte que la zone de texte affichera.
textBox->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc));
System::SharedPtr<Aspose::Words::Paragraph> para = textBox->get_FirstParagraph();
para->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"Hello world!");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(textBox);

doc->Save(get_ArtifactsDir() + u"Shape.CreateTextBox.docx");
```

## Voir aussi

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Enum [ShapeType](../../shapetype/)
* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
