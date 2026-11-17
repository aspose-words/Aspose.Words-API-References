---
title: Aspose::Words::Font::set_Emboss method
linktitle: set_Emboss
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Font::set_Emboss method. True if the font is formatted as embossed in C++.'
type: docs
weight: 67000
url: /cpp/aspose.words/font/set_emboss/
---
## Font::set_Emboss method


True if the font is formatted as embossed.

```cpp
void Aspose::Words::Font::set_Emboss(bool value)
```

## Examples


Shows how to apply engraving/embossing effects to text.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(36);
builder->get_Font()->set_Color(System::Drawing::Color::get_LightBlue());

// Below are two ways of using shadows to apply a 3D-like effect to the text.
// 1 -  Engrave text to make it look like the letters are sunken into the page:
builder->get_Font()->set_Engrave(true);

builder->Writeln(u"This text is engraved.");

// 2 -  Emboss text to make it look like the letters pop out of the page:
builder->get_Font()->set_Engrave(false);
builder->get_Font()->set_Emboss(true);

builder->Writeln(u"This text is embossed.");

doc->Save(get_ArtifactsDir() + u"Font.EngraveEmboss.docx");
```
## See Also

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
