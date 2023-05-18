---
title: Aspose::Words::Font::get_Outline method
linktitle: get_Outline
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Font::get_Outline method. True if the font is formatted as outline in C++.'
type: docs
weight: 31000
url: /cpp/aspose.words/font/get_outline/
---
## Font::get_Outline method


True if the font is formatted as outline.

```cpp
bool Aspose::Words::Font::get_Outline()
```


## Examples



Shows how to create a run of text formatted as outline. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Set the Outline flag to change the text's fill color to white and
// leave a thin outline around each character in the original color of the text.
builder->get_Font()->set_Outline(true);
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Size(36);

builder->Writeln(u"This text has an outline.");

doc->Save(ArtifactsDir + u"Font.Outline.docx");
```

## See Also

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
