---
title: Aspose::Words::DocumentBuilder::PopFont method
linktitle: PopFont
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DocumentBuilder::PopFont method. Retrieves character formatting previously saved on the stack in C++.'
type: docs
weight: 62000
url: /cpp/aspose.words/documentbuilder/popfont/
---
## DocumentBuilder::PopFont method


Retrieves character formatting previously saved on the stack.

```cpp
void Aspose::Words::DocumentBuilder::PopFont()
```


## Examples



Shows how to use a document builder's formatting stack. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Set up font formatting, then write the text that goes before the hyperlink.
builder->get_Font()->set_Name(u"Arial");
builder->get_Font()->set_Size(24);
builder->Write(u"To visit Google, hold Ctrl and click ");

// Preserve our current formatting configuration on the stack.
builder->PushFont();

// Alter the builder's current formatting by applying a new style.
builder->get_Font()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Hyperlink);
builder->InsertHyperlink(u"here", u"http://www.google.com", false);

ASSERT_EQ(System::Drawing::Color::get_Blue().ToArgb(), builder->get_Font()->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Underline::Single, builder->get_Font()->get_Underline());

// Restore the font formatting that we saved earlier and remove the element from the stack.
builder->PopFont();

ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), builder->get_Font()->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Underline::None, builder->get_Font()->get_Underline());

builder->Write(u". We hope you enjoyed the example.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.PushPopFont.docx");
```

## See Also

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
