---
title: Aspose::Words::Font::set_Shadow method
linktitle: set_Shadow
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Font::set_Shadow method. True if the font is formatted as shadowed in C++.'
type: docs
weight: 87000
url: /cpp/aspose.words/font/set_shadow/
---
## Font::set_Shadow method


True if the font is formatted as shadowed.

```cpp
void Aspose::Words::Font::set_Shadow(bool value)
```

## Examples


Shows how to create a run of text formatted with a shadow.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Set the Shadow flag to apply an offset shadow effect,
// making it look like the letters are floating above the page.
builder->get_Font()->set_Shadow(true);
builder->get_Font()->set_Size(36);

builder->Writeln(u"This text has a shadow.");

doc->Save(get_ArtifactsDir() + u"Font.Shadow.docx");
```
## See Also

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
