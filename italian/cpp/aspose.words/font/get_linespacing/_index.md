---
title: "Metodo Aspose::Words::Font::get_LineSpacing"
linktitle: "get_LineSpacing"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Font::get_LineSpacing. Restituisce l'interlinea di questo carattere (in punti) in C++."
type: docs
weight: 21000
url: /it/cpp/aspose.words/font/get_linespacing/
---
## Font::get_LineSpacing method


Restituisce l'interlinea di questo carattere (in punti).

```cpp
double Aspose::Words::Font::get_LineSpacing()
```


## Esempi



Mostra come ottenere l'interlinea di un carattere, in punti.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Imposta caratteri diversi per il DocumentBuilder e verifica la loro interlinea.
builder->get_Font()->set_Name(u"Calibri");
ASPOSE_ASSERT_EQ(14.6484375, builder->get_Font()->get_LineSpacing());

builder->get_Font()->set_Name(u"Times New Roman");
ASPOSE_ASSERT_EQ(13.798828125, builder->get_Font()->get_LineSpacing());
```

## Vedi anche

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
