---
title: "Metodo Aspose::Words::Border::get_Color"
linktitle: "get_Color"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Border::get_Color. Ottiene o imposta il colore del bordo in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words/border/get_color/
---
## Border::get_Color method


Ottiene o imposta il colore del bordo.

```cpp
System::Drawing::Color Aspose::Words::Border::get_Color()
```


## Esempi



Mostra come inserire una stringa circondata da un bordo in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->get_Border()->set_Color(System::Drawing::Color::get_Green());
builder->get_Font()->get_Border()->set_LineWidth(2.5);
builder->get_Font()->get_Border()->set_LineStyle(Aspose::Words::LineStyle::DashDotStroker);

builder->Write(u"Text surrounded by green border.");

doc->Save(get_ArtifactsDir() + u"Border.FontBorder.docx");
```

## Vedi anche

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
