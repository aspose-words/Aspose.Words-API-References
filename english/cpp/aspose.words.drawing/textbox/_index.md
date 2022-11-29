---
title: TextBox
second_title: Aspose.Words for C++ API Reference
description: Defines attributes that specify how a text is displayed inside a shape.
type: docs
weight: 183
url: /cpp/aspose.words.drawing/textbox/
---
## TextBox class


Defines attributes that specify how a text is displayed inside a shape.

```cpp
class TextBox : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [BreakForwardLink](./breakforwardlink/)() | Breaks the link to the next [TextBox](./). |
| [get_FitShapeToText](./get_fitshapetotext/)() | Determines whether Microsoft Word will grow the shape to fit text. |
| [get_InternalMarginBottom](./get_internalmarginbottom/)() | Specifies the inner bottom margin in points for a shape. |
| [get_InternalMarginLeft](./get_internalmarginleft/)() | Specifies the inner left margin in points for a shape. |
| [get_InternalMarginRight](./get_internalmarginright/)() | Specifies the inner right margin in points for a shape. |
| [get_InternalMarginTop](./get_internalmargintop/)() | Specifies the inner top margin in points for a shape. |
| [get_LayoutFlow](./get_layoutflow/)() | Determines the flow of the text layout in a shape. |
| [get_Next](./get_next/)() | Returns or sets a [TextBox](./) that represents the next [TextBox](./) in a sequence of shapes. |
| [get_Parent](./get_parent/)() const | Gets a parent shape for the [TextBox](./). |
| [get_Previous](./get_previous/)() | Returns a [TextBox](./) that represents the previous [TextBox](./) in a sequence of shapes. |
| [get_TextBoxWrapMode](./get_textboxwrapmode/)() | Determines how text wraps inside a shape. |
| [get_VerticalAnchor](./get_verticalanchor/)() | Specifies the vertical alignment of the text within a shape. |
| [IsValidLinkTarget](./isvalidlinktarget/)(const System::SharedPtr\<Aspose::Words::Drawing::TextBox\>\&) | Determines whether this [TextBox](./) can be linked to the target Textbox. |
| [set_FitShapeToText](./set_fitshapetotext/)(bool) | Setter for [Aspose::Words::Drawing::TextBox::get_FitShapeToText](./get_fitshapetotext/). |
| [set_InternalMarginBottom](./set_internalmarginbottom/)(double) | Setter for [Aspose::Words::Drawing::TextBox::get_InternalMarginBottom](./get_internalmarginbottom/). |
| [set_InternalMarginLeft](./set_internalmarginleft/)(double) | Setter for [Aspose::Words::Drawing::TextBox::get_InternalMarginLeft](./get_internalmarginleft/). |
| [set_InternalMarginRight](./set_internalmarginright/)(double) | Setter for [Aspose::Words::Drawing::TextBox::get_InternalMarginRight](./get_internalmarginright/). |
| [set_InternalMarginTop](./set_internalmargintop/)(double) | Setter for [Aspose::Words::Drawing::TextBox::get_InternalMarginTop](./get_internalmargintop/). |
| [set_LayoutFlow](./set_layoutflow/)(Aspose::Words::Drawing::LayoutFlow) | Setter for [Aspose::Words::Drawing::TextBox::get_LayoutFlow](./get_layoutflow/). |
| [set_Next](./set_next/)(const System::SharedPtr\<Aspose::Words::Drawing::TextBox\>\&) | Setter for [Aspose::Words::Drawing::TextBox::get_Next](./get_next/). |
| [set_TextBoxWrapMode](./set_textboxwrapmode/)(Aspose::Words::Drawing::TextBoxWrapMode) | Setter for [Aspose::Words::Drawing::TextBox::get_TextBoxWrapMode](./get_textboxwrapmode/). |
| [set_VerticalAnchor](./set_verticalanchor/)(Aspose::Words::Drawing::TextBoxAnchor) | Setter for [Aspose::Words::Drawing::TextBox::get_VerticalAnchor](./get_verticalanchor/). |
## Remarks


Use the [TextBox](../shape/get_textbox/) property to access text properties of a shape. You do not create instances of the [TextBox](./) class directly.

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


Shows how to get a text box to resize itself to fit its contents tightly. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Shape> textBoxShape = builder->InsertShape(ShapeType::TextBox, 150, 100);
SharedPtr<TextBox> textBox = textBoxShape->get_TextBox();

// Apply these values to both these members to get the parent shape to fit
// tightly around the text contents, ignoring the dimensions we have set.
textBox->set_FitShapeToText(true);
textBox->set_TextBoxWrapMode(TextBoxWrapMode::None);

builder->MoveTo(textBoxShape->get_LastParagraph());
builder->Write(u"Text fit tightly inside textbox.");

doc->Save(ArtifactsDir + u"Shape.TextBoxFitShapeToText.docx");
```


Shows how to set internal margins for a text box. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert another textbox with specific margins.
SharedPtr<Shape> textBoxShape = builder->InsertShape(ShapeType::TextBox, 100, 100);
SharedPtr<TextBox> textBox = textBoxShape->get_TextBox();
textBox->set_InternalMarginTop(15);
textBox->set_InternalMarginBottom(15);
textBox->set_InternalMarginLeft(15);
textBox->set_InternalMarginRight(15);

builder->MoveTo(textBoxShape->get_LastParagraph());
builder->Write(u"Text placed according to textbox margins.");

doc->Save(ArtifactsDir + u"Shape.TextBoxMargins.docx");
```

## See Also

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words](../../)
