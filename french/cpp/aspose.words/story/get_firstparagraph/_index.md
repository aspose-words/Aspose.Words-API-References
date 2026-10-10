---
title: "Méthode Aspose::Words::Story::get_FirstParagraph"
linktitle: "get_FirstParagraph"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Story::get_FirstParagraph. Obtient le premier paragraphe de l’histoire en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words/story/get_firstparagraph/
---
## Story::get_FirstParagraph method


Obtient le premier paragraphe de l'histoire.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::Story::get_FirstParagraph() override
```


## Exemples



Montre comment formater une séquence de texte en utilisant sa propriété de police.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");

System::SharedPtr<Aspose::Words::Font> font = run->get_Font();
font->set_Name(u"Courier New");
font->set_Size(36);
font->set_HighlightColor(System::Drawing::Color::get_Yellow());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);
doc->Save(get_ArtifactsDir() + u"Font.CreateFormattedRun.docx");
```


Montre comment créer et formater une zone de texte.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Créez une zone de texte flottante.
auto textBox = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::TextBox);
textBox->set_WrapType(Aspose::Words::Drawing::WrapType::None);
textBox->set_Height(50);
textBox->set_Width(200);

// Définissez l’alignement horizontal et vertical du texte à l’intérieur de la forme.
textBox->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
textBox->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Top);

// Ajoutez un paragraphe à la zone de texte et ajoutez un segment de texte que la zone de texte affichera.
textBox->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc));
System::SharedPtr<Aspose::Words::Paragraph> para = textBox->get_FirstParagraph();
para->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"Hello world!");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(textBox);

doc->Save(get_ArtifactsDir() + u"Shape.CreateTextBox.docx");
```

## Voir aussi

* Class [Paragraph](../../paragraph/)
* Class [Story](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
