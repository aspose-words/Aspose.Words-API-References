---
title: Aspose::Words::EmphasisMark enum
linktitle: EmphasisMark
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::EmphasisMark enum. Specifies possible types of emphasis mark in C++.'
type: docs
weight: 89000
url: /cpp/aspose.words/emphasismark/
---
## EmphasisMark enum


Specifies possible types of emphasis mark.

```cpp
enum class EmphasisMark
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | 0 | No emphasis mark. |
| OverSolidCircle | 1 | Emphasis mark is a solid black circle displayed above text. |
| OverComma | 2 | Emphasis mark is a comma character displayed above text. |
| OverWhiteCircle | 3 | Emphasis mark is an empty white circle displayed above text. |
| UnderSolidCircle | 4 | Emphasis mark is a solid black circle displayed below text. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
