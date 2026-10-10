---
title: "Aspose::Words::Drawing::Shape::get_TextBox Methode"
linktitle: "get_TextBox"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Shape::get_TextBox Methode. Definiert Attribute, die festlegen, wie Text in einer Form in C++ angezeigt wird."
type: docs
weight: 24000
url: /de/cpp/aspose.words.drawing/shape/get_textbox/
---
## Shape::get_TextBox method


Definiert Attribute, die festlegen, wie Text in einer Form angezeigt wird.

```cpp
System::SharedPtr<Aspose::Words::Drawing::TextBox> Aspose::Words::Drawing::Shape::get_TextBox()
```


## Beispiele



Zeigt, wie die Ausrichtung von Text innerhalb einer Textbox festgelegt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 150, 100);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();

// Bewegen Sie den Dokumenten-Builder in die TextBox und fügen Sie Text hinzu.
builder->MoveTo(textBoxShape->get_LastParagraph());
builder->Writeln(u"Hello world!");
builder->Write(u"Hello again!");

// Setzen Sie die Eigenschaft "LayoutFlow", um eine Ausrichtung für den Textinhalt dieser Textbox festzulegen.
textBox->set_LayoutFlow(layoutFlow);

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxLayoutFlow.docx");
```

## Siehe auch

* Class [TextBox](../../textbox/)
* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
