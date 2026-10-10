---
title: "Aspose::Words::TextEffect-enum"
linktitle: "TextEffect"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::TextEffect-enum. Animeringseffekt för textkörningar i C++."
type: docs
weight: 123000
url: /sv/cpp/aspose.words/texteffect/
---
## TextEffect enum


Animeringseffekt för textkörningar.

```cpp
enum class TextEffect
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| None | 0 |  |
| LasVegasLights | 1 |  |
| BlinkingBackground | 2 |  |
| SparkleText | 3 |  |
| MarchingBlackAnts | 4 |  |
| MarchingRedAnts | 5 |  |
| Shimmer | 6 |  |


## Exempel



Visar hur man tillämpar en visuell effekt på en körning.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(36);
builder->get_Font()->set_TextEffect(Aspose::Words::TextEffect::SparkleText);

builder->Writeln(u"Text with a sparkle effect.");

// Äldre versioner av Microsoft Word stöder endast teckensnittsanimeringseffekter.
doc->Save(get_ArtifactsDir() + u"Font.SparklingText.doc");
```

## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
