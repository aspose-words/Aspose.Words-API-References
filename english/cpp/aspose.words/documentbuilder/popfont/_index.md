---
title: PopFont
second_title: Aspose.Words for C++ API Reference
description: Retrieves character formatting previously saved on the stack.
type: docs
weight: 755
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
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Set up font formatting, then write the text that goes before the hyperlink.
builder->get_Font()->set_Name(u"Arial");
builder->get_Font()->set_Size(24);
builder->Write(u"To visit Google, hold Ctrl and click ");

// Preserve our current formatting configuration on the stack.
builder->PushFont();

// Alter the builder's current formatting by applying a new style.
builder->get_Font()->set_StyleIdentifier(StyleIdentifier::Hyperlink);
builder->InsertHyperlink(u"here", u"http://www.google.com", false);

ASSERT_EQ(System::Drawing::Color::get_Blue().ToArgb(), builder->get_Font()->get_Color().ToArgb());
ASSERT_EQ(Underline::Single, builder->get_Font()->get_Underline());

// Restore the font formatting that we saved earlier and remove the element from the stack.
builder->PopFont();

ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), builder->get_Font()->get_Color().ToArgb());
ASSERT_EQ(Underline::None, builder->get_Font()->get_Underline());

builder->Write(u". We hope you enjoyed the example.");

doc->Save(ArtifactsDir + u"DocumentBuilder.PushPopFont.docx");
```

## See Also

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
