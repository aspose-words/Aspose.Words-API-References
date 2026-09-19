---
title: "Metodo Aspose::Words::Border::get_LineStyle"
linktitle: "get_LineStyle"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Border::get_LineStyle. Ottiene o imposta lo stile del bordo in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words/border/get_linestyle/
---
## Border::get_LineStyle method


Ottiene o imposta lo stile del bordo.

```cpp
Aspose::Words::LineStyle Aspose::Words::Border::get_LineStyle()
```

## Note


Se imposti lo stile della linea su nessuno, la larghezza della linea viene automaticamente impostata a zero.

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

* Enum [LineStyle](../../linestyle/)
* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
