---
title: get_TextBox
second_title: Aspose.Words for C++ API Reference
description: Defines attributes that specify how text is displayed in a shape.
type: docs
weight: 300
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
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Shape> textBoxShape = builder->InsertShape(ShapeType::TextBox, 150, 100);
SharedPtr<TextBox> textBox = textBoxShape->get_TextBox();

// Move the document builder to inside the TextBox and add text.
builder->MoveTo(textBoxShape->get_LastParagraph());
builder->Writeln(u"Hello world!");
builder->Write(u"Hello again!");

// Set the "LayoutFlow" property to set an orientation for the text contents of this text box.
textBox->set_LayoutFlow(layoutFlow);

doc->Save(ArtifactsDir + u"Shape.TextBoxLayoutFlow.docx");
```

## See Also

* Class [TextBox](../../textbox/)
* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words](../../../)
