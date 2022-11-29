---
title: get_LayoutFlow
second_title: Aspose.Words for C++ API Reference
description: Determines the flow of the text layout in a shape.
type: docs
weight: 79
url: /cpp/aspose.words.drawing/textbox/get_layoutflow/
---
## TextBox::get_LayoutFlow method


Determines the flow of the text layout in a shape.

```cpp
Aspose::Words::Drawing::LayoutFlow Aspose::Words::Drawing::TextBox::get_LayoutFlow()
```

## Remarks


The default value is [Horizontal](../../layoutflow/).

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

* Enum [LayoutFlow](../../layoutflow/)
* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words](../../../)
