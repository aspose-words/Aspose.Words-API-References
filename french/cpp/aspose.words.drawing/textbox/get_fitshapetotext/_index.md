---
title: "Aspose::Words::Drawing::TextBox::get_FitShapeToText méthode"
linktitle: "get_FitShapeToText"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::TextBox::get_FitShapeToText méthode. Détermine si Microsoft Word agrandira la forme pour adapter le texte en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.drawing/textbox/get_fitshapetotext/
---
## TextBox::get_FitShapeToText method


Détermine si Microsoft Word agrandira la forme pour s'adapter au texte.

```cpp
bool Aspose::Words::Drawing::TextBox::get_FitShapeToText()
```

## Remarques


La valeur par défaut est **false**.

## Exemples



Montre comment faire en sorte qu'une zone de texte se redimensionne automatiquement pour épouser étroitement son contenu.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 150, 100);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();

// Appliquez ces valeurs aux deux membres pour que la forme parent s'adapte
// étroitement autour du contenu texte, en ignorant les dimensions que nous avons définies.
textBox->set_FitShapeToText(true);
textBox->set_TextBoxWrapMode(Aspose::Words::Drawing::TextBoxWrapMode::None);

builder->MoveTo(textBoxShape->get_LastParagraph());
builder->Write(u"Text fit tightly inside textbox.");

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxFitShapeToText.docx");
```

## Voir aussi

* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
