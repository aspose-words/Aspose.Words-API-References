---
title: "Aspose::Words::TextEffect Aufzählung"
linktitle: "TextEffect"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::TextEffect Aufzählung. Animationseffekt für Textläufe in C++."
type: docs
weight: 123000
url: /de/cpp/aspose.words/texteffect/
---
## TextEffect enum


Animationseffekt für Textläufe.

```cpp
enum class TextEffect
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Keine | 0 |  |
| LasVegasLights | 1 |  |
| BlinkingBackground | 2 |  |
| SparkleText | 3 |  |
| MarchingBlackAnts | 4 |  |
| MarchingRedAnts | 5 |  |
| Shimmer | 6 |  |


## Beispiele



Zeigt, wie ein visueller Effekt auf einen Run angewendet wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(36);
builder->get_Font()->set_TextEffect(Aspose::Words::TextEffect::SparkleText);

builder->Writeln(u"Text with a sparkle effect.");

// Ältere Versionen von Microsoft Word unterstützen nur Schriftart-Animations-Effekte.
doc->Save(get_ArtifactsDir() + u"Font.SparklingText.doc");
```

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
