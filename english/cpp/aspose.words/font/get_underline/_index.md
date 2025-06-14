---
title: Aspose::Words::Font::get_Underline method
linktitle: get_Underline
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Font::get_Underline method. Gets or sets the type of underline applied to the font in C++.'
type: docs
weight: 55000
url: /cpp/aspose.words/font/get_underline/
---
## Font::get_Underline method


Gets or sets the type of underline applied to the font.

```cpp
Aspose::Words::Underline Aspose::Words::Font::get_Underline()
```


## Examples



Shows how to insert formatted text using [DocumentBuilder](../../documentbuilder/). 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Specify font formatting, then add text.
SharedPtr<Aspose::Words::Font> font = builder->get_Font();
font->set_Size(16);
font->set_Bold(true);
font->set_Color(System::Drawing::Color::get_Blue());
font->set_Name(u"Courier New");
font->set_Underline(Underline::Dash);

builder->Write(u"Hello world!");
```


Shows how to configure the style and color of a text underline. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->get_Font()->set_Underline(Underline::Dotted);
builder->get_Font()->set_UnderlineColor(System::Drawing::Color::get_Red());

builder->Writeln(u"Underlined text.");

doc->Save(ArtifactsDir + u"Font.Underlines.docx");
```

## See Also

* Enum [Underline](../../underline/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
