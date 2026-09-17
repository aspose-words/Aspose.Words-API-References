---
title: "Aspose::Words::Drawing::ShapeBase::get_Font méthode"
linktitle: "get_Font"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::ShapeBase::get_Font méthode. Fournit l'accès au format de police de cet objet en C++."
type: docs
weight: 21000
url: /fr/cpp/aspose.words.drawing/shapebase/get_font/
---
## ShapeBase::get_Font method


Fournit l'accès au format de police de cet objet.

```cpp
System::SharedPtr<Aspose::Words::Font> Aspose::Words::Drawing::ShapeBase::get_Font()
```


## Exemples



Montre comment insérer une zone de texte et définir la police de son contenu.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 300, 50);
builder->MoveTo(shape->get_LastParagraph());
builder->Write(u"This text is inside the text box.");

// Définissez la propriété "Hidden" de l'objet "Font" de la forme sur "true" pour masquer la zone de texte à la vue
// et réduire l'espace qu'elle occuperait normalement.
// Définissez la propriété "Hidden" de l'objet "Font" de la forme sur "false" pour laisser la zone de texte visible.
shape->get_Font()->set_Hidden(hideShape);

// Si la forme est visible, nous modifierons son apparence via l'objet font.
if (!hideShape)
{
    shape->get_Font()->set_HighlightColor(System::Drawing::Color::get_LightGray());
    shape->get_Font()->set_Color(System::Drawing::Color::get_Red());
    shape->get_Font()->set_Underline(Aspose::Words::Underline::Dash);
}

// Déplacez le builder hors de la zone de texte vers le document principal.
builder->MoveTo(shape->get_ParentParagraph());

builder->Writeln(u"\nThis text is outside the text box.");

doc->Save(get_ArtifactsDir() + u"Shape.Font.docx");
```

## Voir aussi

* Class [Font](../../../aspose.words/font/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
