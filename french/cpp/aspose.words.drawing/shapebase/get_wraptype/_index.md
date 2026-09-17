---
title: "Aspose::Words::Drawing::ShapeBase::get_WrapType méthode"
linktitle: "get_WrapType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::ShapeBase::get_WrapType méthode. Définit si la forme est en ligne ou flottante. Pour les formes flottantes, définit le mode d'habillage du texte autour de la forme en C++."
type: docs
weight: 56000
url: /fr/cpp/aspose.words.drawing/shapebase/get_wraptype/
---
## ShapeBase::get_WrapType method


Définit si la forme est en ligne ou flottante. Pour les formes flottantes, définit le mode d'habillage du texte autour de la forme.

```cpp
Aspose::Words::Drawing::WrapType Aspose::Words::Drawing::ShapeBase::get_WrapType()
```

## Remarques


La valeur par défaut est [None](../../wraptype/).

N'a d'effet que pour les formes de niveau supérieur.

## Exemples



Montre comment insérer une image flottante au centre d'une page.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez une image flottante qui apparaîtra derrière le texte qui se chevauche et alignez‑la au centre de la page.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
shape->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Center);

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPageCenter.docx");
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

* Enum [WrapType](../../wraptype/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
