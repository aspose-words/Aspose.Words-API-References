---
title: Aspose::Words::Font::get_Shading method
linktitle: get_Shading
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Font::get_Shading method. Returns a Shading object that refers to the shading formatting for the font in C++.'
type: docs
weight: 34000
url: /cpp/aspose.words/font/get_shading/
---
## Font::get_Shading method


Returns a [Shading](../../shading/) object that refers to the shading formatting for the font.

```cpp
System::SharedPtr<Aspose::Words::Shading> Aspose::Words::Font::get_Shading()
```


## Examples



Shows how to apply shading to text created by a document builder. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Color(System::Drawing::Color::get_White());

// One way to make the text created using our white font color visible
// is to apply a background shading effect.
System::SharedPtr<Aspose::Words::Shading> shading = builder->get_Font()->get_Shading();
shading->set_Texture(Aspose::Words::TextureIndex::TextureDiagonalUp);
shading->set_BackgroundPatternColor(System::Drawing::Color::get_OrangeRed());
shading->set_ForegroundPatternColor(System::Drawing::Color::get_DarkBlue());

builder->Writeln(u"White text on an orange background with a two-tone texture.");

doc->Save(get_ArtifactsDir() + u"Font.Shading.docx");
```

## See Also

* Class [Shading](../../shading/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
