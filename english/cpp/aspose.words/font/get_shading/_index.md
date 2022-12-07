---
title: get_Shading
second_title: Aspose.Words for C++ API Reference
description: Returns a Shading object that refers to the shading formatting for the font.
type: docs
weight: 430
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
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->get_Font()->set_Color(System::Drawing::Color::get_White());

// One way to make the text created using our white font color visible
// is to apply a background shading effect.
SharedPtr<Shading> shading = builder->get_Font()->get_Shading();
shading->set_Texture(TextureIndex::TextureDiagonalUp);
shading->set_BackgroundPatternColor(System::Drawing::Color::get_OrangeRed());
shading->set_ForegroundPatternColor(System::Drawing::Color::get_DarkBlue());

builder->Writeln(u"White text on an orange background with a two-tone texture.");

doc->Save(ArtifactsDir + u"Font.Shading.docx");
```

## See Also

* Class [Shading](../../shading/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
