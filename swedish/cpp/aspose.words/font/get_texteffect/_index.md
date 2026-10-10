---
title: "Aspose::Words::Font::get_TextEffect metod"
linktitle: "get_TextEffect"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Font::get_TextEffect metod. Hämtar eller anger teckensnittets animeringseffekt i C++."
type: docs
weight: 47000
url: /sv/cpp/aspose.words/font/get_texteffect/
---
## Font::get_TextEffect method


Hämtar eller anger teckensnittets animeringseffekt.

```cpp
Aspose::Words::TextEffect Aspose::Words::Font::get_TextEffect()
```


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

* Enum [TextEffect](../../texteffect/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
