---
title: "Aspose::Words::Drawing::Shape::Shape costruttore"
linktitle: "Shape"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Shape::Shape costruttore. Crea un nuovo oggetto forma in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.drawing/shape/shape/
---
## Shape::Shape constructor


Crea un nuovo oggetto forma.

```cpp
Aspose::Words::Drawing::Shape::Shape(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, Aspose::Words::Drawing::ShapeType shapeType)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Il documento proprietario. |
| shapeType | Aspose::Words::Drawing::ShapeType | Il tipo della forma da creare. |
## Note


Dovresti specificare le proprietà desiderate della forma dopo aver creato una forma.

## Esempi



Mostra come inserire una forma con un'immagine dal file system locale in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Il costruttore pubblico della classe "Shape" creerà una forma con il tipo di markup "ShapeMarkupLanguage.Vml".
// Se è necessario creare una forma di tipo non primitivo, come SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, o DiagonalCornersRounded,
// Utilizzare DocumentBuilder.InsertShape.
auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Image);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Windows MetaFile.wmf");
shape->set_Width(100);
shape->set_Height(100);

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

doc->Save(get_ArtifactsDir() + u"Image.FromFile.docx");
```


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

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Enum [ShapeType](../../shapetype/)
* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
