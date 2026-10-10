---
title: "Metodo Aspose::Words::Drawing::Shape::get_FirstParagraph"
linktitle: "get_FirstParagraph"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Drawing::Shape::get_FirstParagraph. Ottiene il primo paragrafo nella forma in C++."
type: docs
weight: 8000
url: /it/cpp/aspose.words.drawing/shape/get_firstparagraph/
---
## Shape::get_FirstParagraph method


Ottiene il primo paragrafo nella forma.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::Drawing::Shape::get_FirstParagraph()
```


## Esempi



Mostra come creare e formattare una casella di testo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Crea una casella di testo flottante.
auto textBox = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::TextBox);
textBox->set_WrapType(Aspose::Words::Drawing::WrapType::None);
textBox->set_Height(50);
textBox->set_Width(200);

// Imposta l'allineamento orizzontale e verticale del testo all'interno della forma.
textBox->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
textBox->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Top);

// Aggiungi un paragrafo alla casella di testo e aggiungi una sequenza di testo che la casella di testo visualizzerà.
textBox->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc));
System::SharedPtr<Aspose::Words::Paragraph> para = textBox->get_FirstParagraph();
para->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"Hello world!");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(textBox);

doc->Save(get_ArtifactsDir() + u"Shape.CreateTextBox.docx");
```

## Vedi anche

* Class [Paragraph](../../../aspose.words/paragraph/)
* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
