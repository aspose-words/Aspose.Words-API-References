---
title: get_UnderlineColor
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the color of the underline applied to the font.
type: docs
weight: 716
url: /cpp/aspose.words/font/get_underlinecolor/
---
## Font::get_UnderlineColor method


Gets or sets the color of the underline applied to the font.

```cpp
System::Drawing::Color Aspose::Words::Font::get_UnderlineColor()
```


## Examples



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

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
