---
title: get_TextEffect
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the font animation effect.
type: docs
weight: 599
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
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->get_Font()->set_Size(36);
builder->get_Font()->set_TextEffect(TextEffect::SparkleText);

builder->Writeln(u"Text with a sparkle effect.");

// Older versions of Microsoft Word only support font animation effects.
doc->Save(ArtifactsDir + u"Font.SparklingText.doc");
```

## See Also

* Enum [TextEffect](../../texteffect/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
