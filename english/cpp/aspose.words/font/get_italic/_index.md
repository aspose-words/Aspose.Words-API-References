---
title: Aspose::Words::Font::get_Italic method
linktitle: get_Italic
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Font::get_Italic method. True if the font is formatted as italic in C++.'
type: docs
weight: 18000
url: /cpp/aspose.words/font/get_italic/
---
## Font::get_Italic method


True if the font is formatted as italic.

```cpp
bool Aspose::Words::Font::get_Italic()
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
