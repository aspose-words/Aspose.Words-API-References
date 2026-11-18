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
enum class TextEffect : int
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| BlinkingBackground | 2 |  |
| LasVegasLights | 1 |  |
| MarchingBlackAnts | 4 |  |
| MarchingRedAnts | 5 |  |
| None | 0 |  |
| Shimmer | 6 |  |
| SparkleText | 3 |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
