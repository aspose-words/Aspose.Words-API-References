---
title: Aspose::Words::Drawing::Shape::get_TextBox method
linktitle: get_TextBox
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Shape::get_TextBox method. Defines attributes that specify how text is displayed in a shape in C++.'
type: docs
weight: 24000
url: /cpp/aspose.words.drawing/shape/get_textbox/
---
## Shape::get_TextBox method


Defines attributes that specify how text is displayed in a shape.

```cpp
System::SharedPtr<Aspose::Words::Drawing::TextBox> Aspose::Words::Drawing::Shape::get_TextBox()
```


## Examples



Shows how to set the orientation of text inside a text box. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 150, 100);
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

* Class [TextBox](../../textbox/)
* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
