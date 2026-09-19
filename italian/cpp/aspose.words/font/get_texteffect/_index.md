---
title: "Aspose::Words::Font::get_TextEffect metodo"
linktitle: "get_TextEffect"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Font::get_TextEffect metodo. Ottiene o imposta l'effetto di animazione del carattere in C++."
type: docs
weight: 47000
url: /it/cpp/aspose.words/font/get_texteffect/
---
## Font::get_TextEffect method


Ottiene o imposta l'effetto di animazione del font.

```cpp
Aspose::Words::TextEffect Aspose::Words::Font::get_TextEffect()
```


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

* Enum [TextEffect](../../texteffect/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
