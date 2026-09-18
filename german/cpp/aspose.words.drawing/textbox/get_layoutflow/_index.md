---
title: "Aspose::Words::Drawing::TextBox::get_LayoutFlow-Methode"
linktitle: "get_LayoutFlow"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::TextBox::get_LayoutFlow-Methode. Bestimmt den Fluss des Textlayouts in einer Form in C++."
type: docs
weight: 8000
url: /de/cpp/aspose.words.drawing/textbox/get_layoutflow/
---
## TextBox::get_LayoutFlow method


Bestimmt den Fluss des Textlayouts in einer Form.

```cpp
Aspose::Words::Drawing::LayoutFlow Aspose::Words::Drawing::TextBox::get_LayoutFlow()
```

## Hinweise


Der Standardwert ist [Horizontal](../../layoutflow/).

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

* Enum [LayoutFlow](../../layoutflow/)
* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
