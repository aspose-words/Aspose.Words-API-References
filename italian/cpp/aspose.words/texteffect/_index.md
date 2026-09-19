---
title: "Aspose::Words::TextEffect enum"
linktitle: "TextEffect"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::TextEffect enum. Effetto di animazione per le sequenze di testo in C++."
type: docs
weight: 123000
url: /it/cpp/aspose.words/texteffect/
---
## TextEffect enum


Effetto di animazione per le run di testo.

```cpp
enum class TextEffect
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | 0 |  |
| LasVegasLights | 1 |  |
| BlinkingBackground | 2 |  |
| SparkleText | 3 |  |
| MarchingBlackAnts | 4 |  |
| MarchingRedAnts | 5 |  |
| Shimmer | 6 |  |


## Esempi



Mostra come applicare un effetto visivo a un run.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(36);
builder->get_Font()->set_TextEffect(Aspose::Words::TextEffect::SparkleText);

builder->Writeln(u"Text with a sparkle effect.");

// Le versioni precedenti di Microsoft Word supportano solo effetti di animazione dei caratteri.
doc->Save(get_ArtifactsDir() + u"Font.SparklingText.doc");
```

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
