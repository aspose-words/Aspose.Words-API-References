---
title: "Metodo Aspose::Words::Font::get_Spacing"
linktitle: "get_Spacing"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Font::get_Spacing. Restituisce o imposta la spaziatura (in punti) tra i caratteri in C++."
type: docs
weight: 40000
url: /it/cpp/aspose.words/font/get_spacing/
---
## Font::get_Spacing method


Restituisce o imposta la spaziatura (in punti) tra i caratteri.

```cpp
double Aspose::Words::Font::get_Spacing()
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
