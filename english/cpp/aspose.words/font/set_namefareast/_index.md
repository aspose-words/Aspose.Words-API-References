---
title: Aspose::Words::Font::set_NameFarEast method
linktitle: set_NameFarEast
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Font::set_NameFarEast method. Sets an East Asian font name in C++.'
type: docs
weight: 81000
url: /cpp/aspose.words/font/set_namefareast/
---
## Font::set_NameFarEast method


Sets an East Asian font name.

```cpp
void Aspose::Words::Font::set_NameFarEast(const System::String & value)
```

## Examples


Shows how to insert and format text in a Far East language.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Specify font settings that the document builder will apply to any text that it inserts.
builder->get_Font()->set_Name(u"Courier New");
builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"en-US", false)->get_LCID());

// Name "FarEast" equivalents for our font and locale.
// If the builder inserts Asian characters with this Font configuration, then each run that contains
// these characters will display them using the "FarEast" font/locale instead of the default.
// This could be useful when a western font does not have ideal representations for Asian characters.
builder->get_Font()->set_NameFarEast(u"SimSun");
builder->get_Font()->set_LocaleIdFarEast(System::MakeObject<System::Globalization::CultureInfo>(u"zh-CN", false)->get_LCID());

// This text will be displayed in the default font/locale.
builder->Writeln(u"Hello world!");

// Since these are Asian characters, this run will apply our "FarEast" font/locale equivalents.
builder->Writeln(u"你好世界");

doc->Save(get_ArtifactsDir() + u"Font.FarEast.docx");
```
## See Also

* [Name](../get_name/)

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
