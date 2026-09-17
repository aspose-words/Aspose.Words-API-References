---
title: "Aspose::Words::Drawing::LayoutFlow enum"
linktitle: "LayoutFlow"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::LayoutFlow enum. Détermine le flux de la mise en page du texte dans une zone de texte en C++."
type: docs
weight: 30000
url: /fr/cpp/aspose.words.drawing/layoutflow/
---
## LayoutFlow enum


Détermine le flux de la mise en page du texte dans une zone de texte.

```cpp
enum class LayoutFlow
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Horizontal | 0 | Le texte est affiché horizontalement. |
| TopToBottomIdeographic | 1 | Le texte idéographique est affiché verticalement. |
| BottomToTop | 2 | Le texte est affiché verticalement. |
| TopToBottom | 3 | Le texte est affiché verticalement. |
| HorizontalIdeographic | 4 | Le texte idéographique est affiché horizontalement. |
| Vertical | 5 | Le texte est affiché verticalement. |


## Exemples



Montre comment ajouter du texte à une zone de texte et modifier son orientation.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto textbox = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::TextBox);
textbox->set_Width(100);
textbox->set_Height(100);
textbox->get_TextBox()->set_LayoutFlow(Aspose::Words::Drawing::LayoutFlow::BottomToTop);

textbox->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc));
builder->InsertNode(textbox);

builder->MoveTo(textbox->get_FirstParagraph());
builder->Write(u"This text is flipped 90 degrees to the left.");

doc->Save(get_ArtifactsDir() + u"Drawing.TextBox.docx");
```

## Voir aussi

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
