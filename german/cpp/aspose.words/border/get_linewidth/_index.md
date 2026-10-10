---
title: "Aspose::Words::Border::get_LineWidth Methode"
linktitle: "get_LineWidth"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Border::get_LineWidth Methode. Liest oder setzt die Rahmenbreite in Punkten in C++."
type: docs
weight: 8000
url: /de/cpp/aspose.words/border/get_linewidth/
---
## Border::get_LineWidth method


Liefert oder setzt die Rahmenbreite in Punkten.

```cpp
double Aspose::Words::Border::get_LineWidth()
```

## Hinweise


Wenn Sie die Linienbreite größer als Null setzen, während der Linienstil None ist, wird der Linienstil automatisch auf Einzellinie geändert.

## Beispiele



Zeigt, wie man eine von einem Rahmen umgebene Zeichenkette in ein Dokument einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->get_Border()->set_Color(System::Drawing::Color::get_Green());
builder->get_Font()->get_Border()->set_LineWidth(2.5);
builder->get_Font()->get_Border()->set_LineStyle(Aspose::Words::LineStyle::DashDotStroker);

builder->Write(u"Text surrounded by green border.");

doc->Save(get_ArtifactsDir() + u"Border.FontBorder.docx");
```

## Siehe auch

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
