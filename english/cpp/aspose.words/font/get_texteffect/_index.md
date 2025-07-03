---
title: Aspose::Words::Font::get_TextEffect method
linktitle: get_TextEffect
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Font::get_TextEffect method. Gets or sets the font animation effect in C++.'
type: docs
weight: 47000
url: /cpp/aspose.words/font/get_texteffect/
---
## Font::get_TextEffect method


Gets or sets the font animation effect.

```cpp
Aspose::Words::TextEffect Aspose::Words::Font::get_TextEffect()
```


## Examples



Shows how to apply a visual effect to a run. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(36);
builder->get_Font()->set_TextEffect(Aspose::Words::TextEffect::SparkleText);

builder->Writeln(u"Text with a sparkle effect.");

// Older versions of Microsoft Word only support font animation effects.
doc->Save(get_ArtifactsDir() + u"Font.SparklingText.doc");
```

## See Also

* Enum [TextEffect](../../texteffect/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
