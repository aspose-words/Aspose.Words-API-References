---
title: "Metodo Aspose::Words::Border::get_LineWidth"
linktitle: "get_LineWidth"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Border::get_LineWidth. Ottiene o imposta la larghezza del bordo in punti in C++."
type: docs
weight: 8000
url: /it/cpp/aspose.words/border/get_linewidth/
---
## Border::get_LineWidth method


Ottiene o imposta la larghezza del bordo in punti.

```cpp
double Aspose::Words::Border::get_LineWidth()
```

## Note


Se imposti la larghezza della linea maggiore di zero quando lo stile della linea è nessuno, lo stile della linea viene automaticamente cambiato a linea singola.

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
