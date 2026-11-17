---
title: Aspose::Words::Font::get_Hidden method
linktitle: get_Hidden
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Font::get_Hidden method. True if the font is formatted as hidden text in C++.'
type: docs
weight: 16000
url: /cpp/aspose.words/font/get_hidden/
---
## Font::get_Hidden method


True if the font is formatted as hidden text.

```cpp
bool Aspose::Words::Font::get_Hidden()
```


## Examples



Shows how to create a run of hidden text. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// With the Hidden flag set to true, any text that we create using this Font object will be invisible in the document.
// We will not see or highlight hidden text unless we enable the "Hidden text" option
// found in Microsoft Word via "File" -> "Options" -> "Display". The text will still be there,
// and we will be able to access this text programmatically.
// It is not advised to use this method to hide sensitive information.
builder->get_Font()->set_Hidden(true);
builder->get_Font()->set_Size(36);

builder->Writeln(u"This text will not be visible in the document.");

doc->Save(get_ArtifactsDir() + u"Font.Hidden.docx");
```

## See Also

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
