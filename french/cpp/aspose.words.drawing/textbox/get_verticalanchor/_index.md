---
title: "Aspose::Words::Drawing::TextBox::get_VerticalAnchor méthode"
linktitle: "get_VerticalAnchor"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::TextBox::get_VerticalAnchor méthode. Spécifie l'alignement vertical du texte à l'intérieur d'une forme en C++."
type: docs
weight: 14000
url: /fr/cpp/aspose.words.drawing/textbox/get_verticalanchor/
---
## TextBox::get_VerticalAnchor method


Spécifie l'alignement vertical du texte à l'intérieur d'une forme.

```cpp
Aspose::Words::Drawing::TextBoxAnchor Aspose::Words::Drawing::TextBox::get_VerticalAnchor()
```

## Remarques


La valeur par défaut est [Top](../../textboxanchor/).

## Exemples



Montre comment aligner verticalement le contenu texte d'une zone de texte.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 200, 200);

// Définissez la propriété "VerticalAnchor" sur "TextBoxAnchor.Top" pour
// aligner le texte de cette zone de texte avec le côté supérieur de la forme.
// Définissez la propriété "VerticalAnchor" sur "TextBoxAnchor.Middle" pour
// aligner le texte de cette zone de texte au centre de la forme.
// Définissez la propriété "VerticalAnchor" sur "TextBoxAnchor.Bottom" pour
// aligner le texte de cette zone de texte au bas de la forme.
shape->get_TextBox()->set_VerticalAnchor(verticalAnchor);

builder->MoveTo(shape->get_FirstParagraph());
builder->Write(u"Hello world!");

// L'alignement vertical du texte à l'intérieur des zones de texte est disponible à partir de Microsoft Word 2007.
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2007);
doc->Save(get_ArtifactsDir() + u"Shape.VerticalAnchor.docx");
```

## Voir aussi

* Enum [TextBoxAnchor](../../textboxanchor/)
* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
