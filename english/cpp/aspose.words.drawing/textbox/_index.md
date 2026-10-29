---
title: Aspose::Words::Drawing::TextBox class
linktitle: TextBox
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::TextBox class. Defines attributes that specify how a text is displayed inside a shape. To learn more, visit the Working with Shapes documentation article in C++.'
type: docs
weight: 15000
url: /cpp/aspose.words.drawing/textbox/
---
## TextBox class


Defines attributes that specify how a text is displayed inside a shape. 
To learn more, visit the [Working with Shapes](https://docs.aspose.com/words/cpp/working-with-shapes/) documentation article.

```cpp
class TextBox : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [BreakForwardLink](./breakforwardlink/)() | Breaks the link to the next [TextBox](./). |
| [IsValidLinkTarget](./isvalidlinktarget/)(const System::SharedPtr\<Aspose::Words::Drawing::TextBox\> \&) | Determines whether this [TextBox](./) can be linked to the target [TextBox](./). |
| [get_FitShapeToText](./get_fitshapetotext/)() | Determines whether Microsoft Word will grow the shape to fit text. |
| [get_InternalMarginBottom](./get_internalmarginbottom/)() | Specifies the inner bottom margin in points for a shape. |
| [get_InternalMarginLeft](./get_internalmarginleft/)() | Specifies the inner left margin in points for a shape. |
| [get_InternalMarginRight](./get_internalmarginright/)() | Specifies the inner right margin in points for a shape. |
| [get_InternalMarginTop](./get_internalmargintop/)() | Specifies the inner top margin in points for a shape. |
| [get_LayoutFlow](./get_layoutflow/)() | Determines the flow of the text layout in a shape. |
| [get_Next](./get_next/)() | Returns or sets a [TextBox](./) that represents the next [TextBox](./) in a sequence of shapes. |
| [get_NoTextRotation](./get_notextrotation/)() | Gets or sets a boolean value indicating either text of the TextBox should not rotate when the shape is rotated. |
| [get_Parent](./get_parent/)() const | Gets a parent shape for the [TextBox](./). |
| [get_Previous](./get_previous/)() | Returns a [TextBox](./) that represents the previous [TextBox](./) in a sequence of shapes. |
| [get_TextBoxWrapMode](./get_textboxwrapmode/)() | Determines how text wraps inside a shape. |
| [get_VerticalAnchor](./get_verticalanchor/)() | Specifies the vertical alignment of the text within a shape. |
| [set_FitShapeToText](./set_fitshapetotext/)(bool) | Determines whether Microsoft Word will grow the shape to fit text. |
| [set_InternalMarginBottom](./set_internalmarginbottom/)(double) | Specifies the inner bottom margin in points for a shape. |
| [set_InternalMarginLeft](./set_internalmarginleft/)(double) | Specifies the inner left margin in points for a shape. |
| [set_InternalMarginRight](./set_internalmarginright/)(double) | Specifies the inner right margin in points for a shape. |
| [set_InternalMarginTop](./set_internalmargintop/)(double) | Specifies the inner top margin in points for a shape. |
| [set_LayoutFlow](./set_layoutflow/)(Aspose::Words::Drawing::LayoutFlow) | Determines the flow of the text layout in a shape. |
| [set_Next](./set_next/)(const System::SharedPtr\<Aspose::Words::Drawing::TextBox\> \&) | Sets a [TextBox](./) that represents the next [TextBox](./) in a sequence of shapes. |
| [set_NoTextRotation](./set_notextrotation/)(bool) | Sets a boolean value indicating either text of the TextBox should not rotate when the shape is rotated. |
| [set_TextBoxWrapMode](./set_textboxwrapmode/)(Aspose::Words::Drawing::TextBoxWrapMode) | Determines how text wraps inside a shape. |
| [set_VerticalAnchor](./set_verticalanchor/)(Aspose::Words::Drawing::TextBoxAnchor) | Specifies the vertical alignment of the text within a shape. |
## Remarks


Use the [TextBox](../shape/get_textbox/) property to access text properties of a shape. You do not create instances of the [TextBox](./) class directly.
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

Shows how to get a text box to resize itself to fit its contents tightly.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(ShapeType::TextBox, static_cast<double>(150), static_cast<double>(100));
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();

// Apply these values to both these members to get the parent shape to fit
// tightly around the text contents, ignoring the dimensions we have set.
textBox->set_FitShapeToText(true);
textBox->set_TextBoxWrapMode(TextBoxWrapMode::None);

builder->MoveTo(textBoxShape->get_LastParagraph());
builder->Write(u"Text fit tightly inside textbox.");

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxFitShapeToText.docx");
```

Shows how to set internal margins for a text box.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insert another textbox with specific margins.
System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(ShapeType::TextBox, static_cast<double>(100), static_cast<double>(100));
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();
textBox->set_InternalMarginTop(15);
textBox->set_InternalMarginBottom(15);
textBox->set_InternalMarginLeft(15);
textBox->set_InternalMarginRight(15);

builder->MoveTo(textBoxShape->get_LastParagraph());
builder->Write(u"Text placed according to textbox margins.");

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxMargins.docx");
```
## See Also

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
