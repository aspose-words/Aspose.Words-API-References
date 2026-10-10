---
title: "Aspose::Words::Drawing::TextBoxWrapMode enum"
linktitle: "TextBoxWrapMode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::TextBoxWrapMode enum. Spécifie comment le texte s'enveloppe à l'intérieur d'une forme en C++."
type: docs
weight: 40000
url: /fr/cpp/aspose.words.drawing/textboxwrapmode/
---
## TextBoxWrapMode enum


Spécifie comment le texte s’enroule à l’intérieur d’une forme.

```cpp
enum class TextBoxWrapMode
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Square | 0 | Le texte s'enveloppe à l'intérieur d'une forme. |
| None | 2 | Le texte ne s'enveloppe pas à l'intérieur d'une forme. |


## Exemples



Montre comment définir un mode d'habillage pour le contenu d'une zone de texte.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 300, 300);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();

// Définissez la propriété "TextBoxWrapMode" sur "TextBoxWrapMode.None" pour augmenter la largeur de la zone de texte
// pour accueillir le texte, si elle est suffisamment grande.
// Définissez la propriété "TextBoxWrapMode" sur "TextBoxWrapMode.Square" pour
// envelopper tout le texte à l'intérieur de la zone de texte, en préservant ses dimensions.
textBox->set_TextBoxWrapMode(textBoxWrapMode);

builder->MoveTo(textBoxShape->get_LastParagraph());
builder->get_Font()->set_Size(32);
builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxContentsWrapMode.docx");
```

## Voir aussi

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
