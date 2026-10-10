---
title: "Aspose::Words::Drawing::TextBox::get_LayoutFlow metod"
linktitle: "get_LayoutFlow"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::TextBox::get_LayoutFlow metod. Bestämmer flödet för textlayouten i en form i C++."
type: docs
weight: 8000
url: /sv/cpp/aspose.words.drawing/textbox/get_layoutflow/
---
## TextBox::get_LayoutFlow method


Bestämmer flödet för textlayouten i en form.

```cpp
Aspose::Words::Drawing::LayoutFlow Aspose::Words::Drawing::TextBox::get_LayoutFlow()
```

## Anmärkningar


Standardvärdet är [Horizontal](../../layoutflow/).

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

* Enum [LayoutFlow](../../layoutflow/)
* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
