---
title: "Aspose::Words::Drawing::Shape::get_LastParagraph metod"
linktitle: "get_LastParagraph"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Shape::get_LastParagraph metod. Hämtar det sista stycket i formen i C++."
type: docs
weight: 14000
url: /sv/cpp/aspose.words.drawing/shape/get_lastparagraph/
---
## Shape::get_LastParagraph method


Hämtar det sista stycket i formen.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::Drawing::Shape::get_LastParagraph()
```


## Exempel



Visar hur man ställer in orienteringen av text i en textruta.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 150, 100);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();

// Flytta dokumentbyggaren in i TextBox och lägg till text.
builder->MoveTo(textBoxShape->get_LastParagraph());
builder->Writeln(u"Hello world!");
builder->Write(u"Hello again!");

// Ställ in egenskapen "LayoutFlow" för att ange en orientering för textinnehållet i den här textrutan.
textBox->set_LayoutFlow(layoutFlow);

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxLayoutFlow.docx");
```

## Se även

* Class [Paragraph](../../../aspose.words/paragraph/)
* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
