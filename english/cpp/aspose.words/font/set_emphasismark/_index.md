---
title: Aspose::Words::Font::set_EmphasisMark method
linktitle: set_EmphasisMark
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Font::set_EmphasisMark method. Sets the emphasis mark applied to this formatting in C++.'
type: docs
weight: 68000
url: /cpp/aspose.words/font/set_emphasismark/
---
## Font::set_EmphasisMark method


Sets the emphasis mark applied to this formatting.

```cpp
void Aspose::Words::Font::set_EmphasisMark(Aspose::Words::EmphasisMark value)
```

## Examples


Shows how to add additional character rendered above/below the glyph-character.

```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

// Possible types of emphasis mark:
// https://apireference.aspose.com/words/net/aspose.words/emphasismark
builder->get_Font()->set_EmphasisMark(emphasisMark);

builder->Write(u"Emphasis text");
builder->Writeln();
builder->get_Font()->ClearFormatting();
builder->Write(u"Simple text");

builder->get_Document()->Save(get_ArtifactsDir() + u"Fonts.SetEmphasisMark.docx");
```
## See Also

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
