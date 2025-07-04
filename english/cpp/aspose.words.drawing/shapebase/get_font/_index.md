---
title: Aspose::Words::Drawing::ShapeBase::get_Font method
linktitle: get_Font
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::ShapeBase::get_Font method. Provides access to the font formatting of this object in C++.'
type: docs
weight: 21000
url: /cpp/aspose.words.drawing/shapebase/get_font/
---
## ShapeBase::get_Font method


Provides access to the font formatting of this object.

```cpp
System::SharedPtr<Aspose::Words::Font> Aspose::Words::Drawing::ShapeBase::get_Font()
```


## Examples



Shows how to insert a text box, and set the font of its contents. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 300, 50);
builder->MoveTo(shape->get_LastParagraph());
builder->Write(u"This text is inside the text box.");

// Set the "Hidden" property of the shape's "Font" object to "true" to hide the text box from sight
// and collapse the space that it would normally occupy.
// Set the "Hidden" property of the shape's "Font" object to "false" to leave the text box visible.
shape->get_Font()->set_Hidden(hideShape);

// If the shape is visible, we will modify its appearance via the font object.
if (!hideShape)
{
    shape->get_Font()->set_HighlightColor(System::Drawing::Color::get_LightGray());
    shape->get_Font()->set_Color(System::Drawing::Color::get_Red());
    shape->get_Font()->set_Underline(Aspose::Words::Underline::Dash);
}

// Move the builder out of the text box back into the main document.
builder->MoveTo(shape->get_ParentParagraph());

builder->Writeln(u"\nThis text is outside the text box.");

doc->Save(get_ArtifactsDir() + u"Shape.Font.docx");
```

## See Also

* Class [Font](../../../aspose.words/font/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
