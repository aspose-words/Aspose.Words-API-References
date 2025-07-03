---
title: Aspose::Words::Font::get_Kerning method
linktitle: get_Kerning
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Font::get_Kerning method. Gets or sets the font size at which kerning starts in C++.'
type: docs
weight: 20000
url: /cpp/aspose.words/font/get_kerning/
---
## Font::get_Kerning method


Gets or sets the font size at which kerning starts.

```cpp
double Aspose::Words::Font::get_Kerning()
```


## Examples



Shows how to specify the font size at which kerning begins to take effect. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_Font()->set_Name(u"Arial Black");

// Set the builder's font size, and minimum size at which kerning will take effect.
// The font size falls below the kerning threshold, so the run bellow will not have kerning.
builder->get_Font()->set_Size(18);
builder->get_Font()->set_Kerning(24);

builder->Writeln(u"TALLY. (Kerning not applied)");

// Set the kerning threshold so that the builder's current font size is above it.
// Any text we add from this point will have kerning applied. The spaces between characters
// will be adjusted, normally resulting in a slightly more aesthetically pleasing text run.
builder->get_Font()->set_Kerning(12);

builder->Writeln(u"TALLY. (Kerning applied)");

doc->Save(get_ArtifactsDir() + u"Font.Kerning.docx");
```

## See Also

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
