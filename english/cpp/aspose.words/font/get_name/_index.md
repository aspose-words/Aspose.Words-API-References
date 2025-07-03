---
title: Aspose::Words::Font::get_Name method
linktitle: get_Name
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Font::get_Name method. Gets or sets the name of the font in C++.'
type: docs
weight: 25000
url: /cpp/aspose.words/font/get_name/
---
## Font::get_Name method


Gets or sets the name of the font.

```cpp
System::String Aspose::Words::Font::get_Name()
```

## Remarks


When getting, returns [NameAscii](../get_nameascii/).

When setting, sets [NameAscii](../get_nameascii/), [NameBi](../get_namebi/), [NameFarEast](../get_namefareast/) and [NameOther](../get_nameother/) to the specified value.

## Examples



Shows how to insert formatted text using [DocumentBuilder](../../documentbuilder/). 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Specify font formatting, then add text.
System::SharedPtr<Aspose::Words::Font> font = builder->get_Font();
font->set_Size(16);
font->set_Bold(true);
font->set_Color(System::Drawing::Color::get_Blue());
font->set_Name(u"Courier New");
font->set_Underline(Aspose::Words::Underline::Dash);

builder->Write(u"Hello world!");
```


Shows how to format a run of text using its font property. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");

System::SharedPtr<Aspose::Words::Font> font = run->get_Font();
font->set_Name(u"Courier New");
font->set_Size(36);
font->set_HighlightColor(System::Drawing::Color::get_Yellow());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);
doc->Save(get_ArtifactsDir() + u"Font.CreateFormattedRun.docx");
```

## See Also

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
