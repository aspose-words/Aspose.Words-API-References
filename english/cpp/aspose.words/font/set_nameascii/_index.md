---
title: Aspose::Words::Font::set_NameAscii method
linktitle: set_NameAscii
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Font::set_NameAscii method. Sets the font used for Latin text (characters with character codes from 0 (zero) through 127) in C++.'
type: docs
weight: 79000
url: /cpp/aspose.words/font/set_nameascii/
---
## Font::set_NameAscii method


Sets the font used for Latin text (characters with character codes from 0 (zero) through 127).

```cpp
void Aspose::Words::Font::set_NameAscii(const System::String & value)
```

## Examples


Shows how Microsoft Word can combine two different fonts in one run.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Suppose a run that we use the builder to insert while using this font configuration
// contains characters within the ASCII characters' range. In that case,
// it will display those characters using this font.
builder->get_Font()->set_NameAscii(u"Calibri");

// With no other font specified, the builder will also apply this font to all characters that it inserts.
ASSERT_EQ(u"Calibri", builder->get_Font()->get_Name());

// Specify a font to use for all characters outside of the ASCII range.
// Ideally, this font should have a glyph for each required non-ASCII character code.
builder->get_Font()->set_NameOther(u"Courier New");

// Insert a run with one word consisting of ASCII characters, and one word with all characters outside that range.
// Each character will be displayed using either of the fonts, depending on.
builder->Writeln(u"Hello, Привет");

doc->Save(get_ArtifactsDir() + u"Font.NameAscii.docx");
```
## See Also

* [Name](../get_name/)

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
