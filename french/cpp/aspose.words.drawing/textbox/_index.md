---
title: "Aspose::Words::Drawing::TextBox class"
linktitle: "ZoneDeTexte"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::TextBox class. Définit les attributs qui spécifient comment un texte est affiché à l'intérieur d'une forme. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 15000
url: /fr/cpp/aspose.words.drawing/textbox/
---
## TextBox class


Définit les attributs qui spécifient comment un texte est affiché à l'intérieur d'une forme. Pour en savoir plus, consultez l'article de documentation [Working with Shapes](https://docs.aspose.com/words/cpp/working-with-shapes/) .

```cpp
class TextBox : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [BreakForwardLink](./breakforwardlink/)() | Rompt le lien vers le prochain [TextBox](./). |
| [get_FitShapeToText](./get_fitshapetotext/)() | Détermine si Microsoft Word agrandira la forme pour s'adapter au texte. |
| [get_InternalMarginBottom](./get_internalmarginbottom/)() | Spécifie la marge intérieure inférieure en points pour une forme. |
| [get_InternalMarginLeft](./get_internalmarginleft/)() | Spécifie la marge intérieure gauche en points pour une forme. |
| [get_InternalMarginRight](./get_internalmarginright/)() | Spécifie la marge intérieure droite en points pour une forme. |
| [get_InternalMarginTop](./get_internalmargintop/)() | Spécifie la marge intérieure supérieure en points pour une forme. |
| [get_LayoutFlow](./get_layoutflow/)() | Détermine le flux de la mise en page du texte dans une forme. |
| [get_Next](./get_next/)() | Renvoie ou définit un [TextBox](./) qui représente le prochain [TextBox](./) dans une séquence de formes. |
| [get_NoTextRotation](./get_notextrotation/)() | Obtient ou définit une valeur booléenne indiquant que le texte du [TextBox](./) ne doit pas pivoter lorsque la forme est tournée. |
| [get_Parent](./get_parent/)() const | Obtient une forme parent pour le [TextBox](./). |
| [get_Previous](./get_previous/)() | Renvoie un [TextBox](./) qui représente le [TextBox](./) précédent dans une séquence de formes. |
| [get_TextBoxWrapMode](./get_textboxwrapmode/)() | Détermine comment le texte s'enroule à l'intérieur d'une forme. |
| [get_VerticalAnchor](./get_verticalanchor/)() | Spécifie l'alignement vertical du texte à l'intérieur d'une forme. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsValidLinkTarget](./isvalidlinktarget/)(const System::SharedPtr\<Aspose::Words::Drawing::TextBox\>\&) | Détermine si ce [TextBox](./) peut être lié au [TextBox](./) cible. |
| [set_FitShapeToText](./set_fitshapetotext/)(bool) | Définisseur pour [Aspose::Words::Drawing::TextBox::get_FitShapeToText](./get_fitshapetotext/). |
| [set_InternalMarginBottom](./set_internalmarginbottom/)(double) | Définisseur pour [Aspose::Words::Drawing::TextBox::get_InternalMarginBottom](./get_internalmarginbottom/). |
| [set_InternalMarginLeft](./set_internalmarginleft/)(double) | Définisseur pour [Aspose::Words::Drawing::TextBox::get_InternalMarginLeft](./get_internalmarginleft/). |
| [set_InternalMarginRight](./set_internalmarginright/)(double) | Définisseur pour [Aspose::Words::Drawing::TextBox::get_InternalMarginRight](./get_internalmarginright/). |
| [set_InternalMarginTop](./set_internalmargintop/)(double) | Définisseur pour [Aspose::Words::Drawing::TextBox::get_InternalMarginTop](./get_internalmargintop/). |
| [set_LayoutFlow](./set_layoutflow/)(Aspose::Words::Drawing::LayoutFlow) | Définisseur pour [Aspose::Words::Drawing::TextBox::get_LayoutFlow](./get_layoutflow/). |
| [set_Next](./set_next/)(const System::SharedPtr\<Aspose::Words::Drawing::TextBox\>\&) | Définisseur pour [Aspose::Words::Drawing::TextBox::get_Next](./get_next/). |
| [set_NoTextRotation](./set_notextrotation/)(bool) | Définisseur pour [Aspose::Words::Drawing::TextBox::get_NoTextRotation](./get_notextrotation/). |
| [set_TextBoxWrapMode](./set_textboxwrapmode/)(Aspose::Words::Drawing::TextBoxWrapMode) | Définisseur pour [Aspose::Words::Drawing::TextBox::get_TextBoxWrapMode](./get_textboxwrapmode/). |
| [set_VerticalAnchor](./set_verticalanchor/)(Aspose::Words::Drawing::TextBoxAnchor) | Définisseur pour [Aspose::Words::Drawing::TextBox::get_VerticalAnchor](./get_verticalanchor/). |
| static [Type](./type/)() |  |
## Remarques


Utilisez la propriété [TextBox](../shape/get_textbox/) pour accéder aux propriétés de texte d'une forme. Vous ne créez pas d'instances de la classe [TextBox](./) directement.

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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
