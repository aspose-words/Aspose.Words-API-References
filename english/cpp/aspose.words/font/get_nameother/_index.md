---
title: get_NameOther
second_title: Aspose.Words for C++ API Reference
description: Returns or sets the font used for characters with character codes from 128 through 255.
type: docs
weight: 352
url: /cpp/aspose.words/font/get_nameother/
---
## Font.get_NameOther method


Returns or sets the font used for characters with character codes from 128 through 255.

```cpp
System::String Aspose::Words::Font::get_NameOther()
```


## Examples




Shows how Microsoft Word can combine two different fonts in one run. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

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

doc->Save(ArtifactsDir + u"Font.NameAscii.docx");
```

