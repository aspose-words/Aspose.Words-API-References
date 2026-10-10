---
title: "Aspose::Words::Drawing::Shape::get_TextBox metod"
linktitle: "get_TextBox"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Shape::get_TextBox metod. Definierar attribut som specificerar hur text visas i en form i C++."
type: docs
weight: 24000
url: /sv/cpp/aspose.words.drawing/shape/get_textbox/
---
## Shape::get_TextBox method


Definierar attribut som anger hur text visas i en form.

```cpp
System::SharedPtr<Aspose::Words::Drawing::TextBox> Aspose::Words::Drawing::Shape::get_TextBox()
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

* Class [TextBox](../../textbox/)
* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
