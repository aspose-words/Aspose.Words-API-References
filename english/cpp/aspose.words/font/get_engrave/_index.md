---
title: get_Engrave
second_title: Aspose.Words for C++ API Reference
description: True if the font is formatted as engraved.
type: docs
weight: 157
url: /cpp/aspose.words/font/get_engrave/
---
## Font.get_Engrave method


True if the font is formatted as engraved.

```cpp
bool Aspose::Words::Font::get_Engrave()
```


## Examples




Shows how to apply engraving/embossing effects to text. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

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

doc->Save(ArtifactsDir + u"Font.EngraveEmboss.docx");
```

