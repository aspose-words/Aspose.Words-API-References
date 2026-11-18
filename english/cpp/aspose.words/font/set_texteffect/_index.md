---
title: Aspose::Words::Font::set_TextEffect method
linktitle: set_TextEffect
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Font::set_TextEffect method. Sets the font animation effect in C++.'
type: docs
weight: 99000
url: /cpp/aspose.words/font/set_texteffect/
---
## Font::set_TextEffect method


Sets the font animation effect.

```cpp
void Aspose::Words::Font::set_TextEffect(Aspose::Words::TextEffect value)
```

## Examples


Shows how to apply a visual effect to a run.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(36);
builder->get_Font()->set_TextEffect(TextEffect::SparkleText);

builder->Writeln(u"Text with a sparkle effect.");

// Older versions of Microsoft Word only support font animation effects.
doc->Save(get_ArtifactsDir() + u"Font.SparklingText.doc");
```
## See Also

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
