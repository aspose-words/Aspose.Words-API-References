---
title: "Méthode Aspose::Words::Drawing::TextBox::get_InternalMarginLeft"
linktitle: "get_InternalMarginLeft"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Drawing::TextBox::get_InternalMarginLeft. Spécifie la marge intérieure gauche en points pour une forme en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.drawing/textbox/get_internalmarginleft/
---
## TextBox::get_InternalMarginLeft method


Spécifie la marge intérieure gauche en points pour une forme.

```cpp
double Aspose::Words::Drawing::TextBox::get_InternalMarginLeft()
```

## Remarques


La valeur par défaut est 1/10 pouce.

## Exemples



Montre comment définir les marges internes d'une zone de texte.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez une autre zone de texte avec des marges spécifiques.
System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 100, 100);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();
textBox->set_InternalMarginTop(15);
textBox->set_InternalMarginBottom(15);
textBox->set_InternalMarginLeft(15);
textBox->set_InternalMarginRight(15);

builder->MoveTo(textBoxShape->get_LastParagraph());
builder->Write(u"Text placed according to textbox margins.");

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxMargins.docx");
```

## Voir aussi

* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
