---
title: get_EmphasisMark
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the emphasis mark applied to this formatting.
type: docs
weight: 144
url: /cpp/aspose.words/font/get_emphasismark/
---
## Font.get_EmphasisMark method


Gets or sets the emphasis mark applied to this formatting.

```cpp
Aspose::Words::EmphasisMark Aspose::Words::Font::get_EmphasisMark()
```


## Examples




Shows how to add additional character rendered above/below the glyph-character. 
```cpp
auto builder = MakeObject<DocumentBuilder>();

// Possible types of emphasis mark:
// https://apireference.aspose.com/words/net/aspose.words/emphasismark
builder->get_Font()->set_EmphasisMark(emphasisMark);

builder->Write(u"Emphasis text");
builder->Writeln();
builder->get_Font()->ClearFormatting();
builder->Write(u"Simple text");

builder->get_Document()->Save(ArtifactsDir + u"Fonts.SetEmphasisMark.docx");
```

