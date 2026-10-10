---
title: "Aspose::Words::Font::get_TextEffect Methode"
linktitle: "get_TextEffect"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Font::get_TextEffect Methode. Ruft den Schriftanimationseffekt in C++ ab oder legt ihn fest."
type: docs
weight: 47000
url: /de/cpp/aspose.words/font/get_texteffect/
---
## Font::get_TextEffect method


Liest oder legt den Schriftanimationseffekt fest.

```cpp
Aspose::Words::TextEffect Aspose::Words::Font::get_TextEffect()
```


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

* Enum [TextEffect](../../texteffect/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
