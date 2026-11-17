---
title: Aspose::Words::Font::get_BoldBi method
linktitle: get_BoldBi
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Font::get_BoldBi method. True if the right-to-left text is formatted as bold in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words/font/get_boldbi/
---
## Font::get_BoldBi method


True if the right-to-left text is formatted as bold.

```cpp
bool Aspose::Words::Font::get_BoldBi()
```


## Examples



Shows how to define separate sets of font settings for right-to-left, and right-to-left text. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Define a set of font settings for left-to-right text.
builder->get_Font()->set_Name(u"Courier New");
builder->get_Font()->set_Size(16);
builder->get_Font()->set_Italic(false);
builder->get_Font()->set_Bold(false);
builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"en-US", false)->get_LCID());

// Define another set of font settings for right-to-left text.
builder->get_Font()->set_NameBi(u"Andalus");
builder->get_Font()->set_SizeBi(24);
builder->get_Font()->set_ItalicBi(true);
builder->get_Font()->set_BoldBi(true);
builder->get_Font()->set_LocaleIdBi(System::MakeObject<System::Globalization::CultureInfo>(u"ar-AR", false)->get_LCID());

// We can use the Bidi flag to indicate whether the text we are about to add
// with the document builder is right-to-left. When we add text with this flag set to true,
// it will be formatted using the right-to-left set of font settings.
builder->get_Font()->set_Bidi(true);
builder->Write(u"مرحبًا");

// Set the flag to false, and then add left-to-right text.
// The document builder will format these using the left-to-right set of font settings.
builder->get_Font()->set_Bidi(false);
builder->Write(u" Hello world!");

doc->Save(get_ArtifactsDir() + u"Font.Bidi.docx");
```

## See Also

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
