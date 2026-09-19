---
title: "Aspose::Words::Font::get_Scaling metodo"
linktitle: "get_Scaling"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Font::get_Scaling metodo. Ottiene o imposta la scala della larghezza dei caratteri in percentuale in C++."
type: docs
weight: 33000
url: /it/cpp/aspose.words/font/get_scaling/
---
## Font::get_Scaling method


Ottiene o imposta la scala della larghezza dei caratteri in percentuale.

```cpp
int32_t Aspose::Words::Font::get_Scaling()
```


## Esempi



Mostra come impostare la scala orizzontale e la spaziatura per i caratteri.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Aggiungi un blocco di testo e aumenta la larghezza dei caratteri al 150%.
builder->get_Font()->set_Scaling(150);
builder->Writeln(u"Wide characters");

// Aggiungi un blocco di testo e aggiungi 1 pt di spaziatura orizzontale extra tra ogni carattere.
builder->get_Font()->set_Spacing(1);
builder->Writeln(u"Expanded by 1pt");

// Aggiungi un blocco di testo e avvicina i caratteri di 1 pt.
builder->get_Font()->set_Spacing(-1);
builder->Writeln(u"Condensed by 1pt");

doc->Save(get_ArtifactsDir() + u"Font.ScalingSpacing.docx");
```

## Vedi anche

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
