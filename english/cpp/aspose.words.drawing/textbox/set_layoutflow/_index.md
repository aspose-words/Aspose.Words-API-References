---
title: Aspose::Words::Drawing::TextBox::set_LayoutFlow method
linktitle: set_LayoutFlow
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::TextBox::set_LayoutFlow method. Determines the flow of the text layout in a shape in C++.'
type: docs
weight: 23000
url: /cpp/aspose.words.drawing/textbox/set_layoutflow/
---
## TextBox::set_LayoutFlow method


Determines the flow of the text layout in a shape.

```cpp
void Aspose::Words::Drawing::TextBox::set_LayoutFlow(Aspose::Words::Drawing::LayoutFlow value)
```

## Remarks


The default value is [Horizontal](../../layoutflow/).
## Examples


Shows how to set the orientation of text inside a text box.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(ShapeType::TextBox, static_cast<double>(150), static_cast<double>(100));
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();

// Move the document builder to inside the TextBox and add text.
builder->MoveTo(textBoxShape->get_LastParagraph());
builder->Writeln(u"Hello world!");
builder->Write(u"Hello again!");

// Set the "LayoutFlow" property to set an orientation for the text contents of this text box.
textBox->set_LayoutFlow(layoutFlow);

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxLayoutFlow.docx");
```
## See Also

* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
