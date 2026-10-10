---
title: "Aspose::Words::Story::get_FirstParagraph Methode"
linktitle: "get_FirstParagraph"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Story::get_FirstParagraph Methode. Gibt den ersten Absatz der Story in C++ zurück."
type: docs
weight: 4000
url: /de/cpp/aspose.words/story/get_firstparagraph/
---
## Story::get_FirstParagraph method


Ermittelt den ersten Absatz in der Geschichte.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::Story::get_FirstParagraph() override
```


## Beispiele



Zeigt, wie man einen Text‑Run mit seiner Schriftarteigenschaft formatiert.
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


Zeigt, wie man ein Textfeld erstellt und formatiert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Erstelle ein schwebendes Textfeld.
auto textBox = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::TextBox);
textBox->set_WrapType(Aspose::Words::Drawing::WrapType::None);
textBox->set_Height(50);
textBox->set_Width(200);

// Lege die horizontale und vertikale Ausrichtung des Textes innerhalb der Form fest.
textBox->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
textBox->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Top);

// Füge dem Textfeld einen Absatz hinzu und füge einen Textlauf hinzu, den das Textfeld anzeigen soll.
textBox->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc));
System::SharedPtr<Aspose::Words::Paragraph> para = textBox->get_FirstParagraph();
para->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"Hello world!");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(textBox);

doc->Save(get_ArtifactsDir() + u"Shape.CreateTextBox.docx");
```

## Siehe auch

* Class [Paragraph](../../paragraph/)
* Class [Story](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
