---
title: "Méthode Aspose::Words::Drawing::Shape::get_TextBox"
linktitle: "get_TextBox"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Drawing::Shape::get_TextBox. Définit les attributs qui spécifient comment le texte est affiché dans une forme en C++."
type: docs
weight: 24000
url: /fr/cpp/aspose.words.drawing/shape/get_textbox/
---
## Shape::get_TextBox method


Définit les attributs qui spécifient comment le texte est affiché dans une forme.

```cpp
System::SharedPtr<Aspose::Words::Drawing::TextBox> Aspose::Words::Drawing::Shape::get_TextBox()
```


## Exemples



Montre comment définir l'orientation du texte à l'intérieur d'une zone de texte.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 150, 100);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();

// Déplacez le générateur de document à l'intérieur du TextBox et ajoutez du texte.
builder->MoveTo(textBoxShape->get_LastParagraph());
builder->Writeln(u"Hello world!");
builder->Write(u"Hello again!");

// Définissez la propriété "LayoutFlow" pour définir une orientation du contenu texte de cette zone de texte.
textBox->set_LayoutFlow(layoutFlow);

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxLayoutFlow.docx");
```

## Voir aussi

* Class [TextBox](../../textbox/)
* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
