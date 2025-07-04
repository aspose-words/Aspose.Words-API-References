---
title: Aspose::Words::TextEffect enum
linktitle: TextEffect
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::TextEffect enum. Animation effect for text runs in C++.'
type: docs
weight: 123000
url: /cpp/aspose.words/texteffect/
---
## TextEffect enum


Animation effect for text runs.

```cpp
enum class TextEffect
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | 0 |  |
| LasVegasLights | 1 |  |
| BlinkingBackground | 2 |  |
| SparkleText | 3 |  |
| MarchingBlackAnts | 4 |  |
| MarchingRedAnts | 5 |  |
| Shimmer | 6 |  |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
