---
title: "Aspose::Words::Drawing::TextBoxAnchor enum"
linktitle: "TextBoxAnchor"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::TextBoxAnchor enum. Spécifie les valeurs utilisées pour l'alignement vertical du texte de forme en C++."
type: docs
weight: 39000
url: /fr/cpp/aspose.words.drawing/textboxanchor/
---
## TextBoxAnchor enum


Spécifie les valeurs utilisées pour l’alignement vertical du texte de forme.

```cpp
enum class TextBoxAnchor
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Top | 0 | Le texte est aligné en haut de la zone de texte. |
| Middle | 1 | Le texte est aligné au milieu de la zone de texte. |
| Bottom | 2 | Le texte est aligné en bas de la zone de texte. |
| TopCentered | 3 | Le texte est aligné en haut centré de la zone de texte. |
| MiddleCentered | 4 | Le texte est aligné au milieu centré de la zone de texte. |
| BottomCentered | 5 | Le texte est aligné en bas centré de la zone de texte. |
| TopBaseline | 6 | Le texte est aligné sur la ligne de base supérieure de la zone de texte. |
| BottomBaseline | 7 | Le texte est aligné sur la ligne de base inférieure de la zone de texte. |
| TopCenteredBaseline | 8 | Le texte est aligné sur la ligne de base centrée supérieure de la zone de texte. |
| BottomCenteredBaseline | 9 | Le texte est aligné sur la ligne de base centrée inférieure de la zone de texte. |


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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
