---
title: "Metodo Aspose::Words::Font::get_Kerning"
linktitle: "get_Kerning"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Font::get_Kerning. Ottiene o imposta la dimensione del carattere a cui inizia il kerning in C++."
type: docs
weight: 20000
url: /it/cpp/aspose.words/font/get_kerning/
---
## Font::get_Kerning method


Ottiene o imposta la dimensione del carattere a partire dalla quale inizia il kerning.

```cpp
double Aspose::Words::Font::get_Kerning()
```


## Esempi



Mostra come specificare la dimensione del carattere a cui il kerning inizia a fare effetto.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_Font()->set_Name(u"Arial Black");

// Imposta la dimensione del carattere del builder e la dimensione minima a cui il kerning avrà effetto.
// La dimensione del carattere scende sotto la soglia del kerning, quindi la sequenza sottostante non avrà kerning.
builder->get_Font()->set_Size(18);
builder->get_Font()->set_Kerning(24);

builder->Writeln(u"TALLY. (Kerning not applied)");

// Imposta la soglia del kerning in modo che la dimensione attuale del carattere del builder sia superiore ad essa.
// Qualsiasi testo aggiunto da questo punto avrà il kerning applicato. Gli spazi tra i caratteri
// saranno regolati, risultando normalmente in una sequenza di testo leggermente più estetica.
builder->get_Font()->set_Kerning(12);

builder->Writeln(u"TALLY. (Kerning applied)");

doc->Save(get_ArtifactsDir() + u"Font.Kerning.docx");
```

## Vedi anche

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
