---
title: Aspose::Words::Font::set_Italic method
linktitle: set_Italic
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Font::set_Italic method. True if the font is formatted as italic in C++.'
type: docs
weight: 72000
url: /cpp/aspose.words/font/set_italic/
---
## Font::set_Italic method


True if the font is formatted as italic.

```cpp
void Aspose::Words::Font::set_Italic(bool value)
```

## Examples


Shows how to write italicized text using a document builder.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(36);
builder->get_Font()->set_Italic(true);
builder->Writeln(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"Font.Italic.docx");
```
## See Also

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
