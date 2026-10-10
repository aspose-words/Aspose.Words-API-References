---
title: "Aspose::Words::Drawing::TextBox::get_LayoutFlow méthode"
linktitle: "get_LayoutFlow"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::TextBox::get_LayoutFlow méthode. Détermine le flux de la mise en page du texte dans une forme en C++."
type: docs
weight: 8000
url: /fr/cpp/aspose.words.drawing/textbox/get_layoutflow/
---
## TextBox::get_LayoutFlow method


Détermine le flux de la mise en page du texte dans une forme.

```cpp
Aspose::Words::Drawing::LayoutFlow Aspose::Words::Drawing::TextBox::get_LayoutFlow()
```

## Remarques


La valeur par défaut est [Horizontal](../../layoutflow/).

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

* Enum [LayoutFlow](../../layoutflow/)
* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
