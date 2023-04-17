---
title: Aspose::Words::Font::get_Size method
linktitle: get_Size
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Font::get_Size method. Gets or sets the font size in points in C++.'
type: docs
weight: 36000
url: /cpp/aspose.words/font/get_size/
---
## Font::get_Size method


Gets or sets the font size in points.

```cpp
double Aspose::Words::Font::get_Size()
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


Shows how to format a run of text using its font property. 
```cpp
auto doc = MakeObject<Document>();
auto run = MakeObject<Run>(doc, u"Hello world!");

SharedPtr<Aspose::Words::Font> font = run->get_Font();
font->set_Name(u"Courier New");
font->set_Size(36);
font->set_HighlightColor(System::Drawing::Color::get_Yellow());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild(run);
doc->Save(ArtifactsDir + u"Font.CreateFormattedRun.docx");
```

## See Also

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
