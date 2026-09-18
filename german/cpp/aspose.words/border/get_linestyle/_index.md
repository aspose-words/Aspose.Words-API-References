---
title: "Aspose::Words::Border::get_LineStyle Methode"
linktitle: "get_LineStyle"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Border::get_LineStyle Methode. Liest oder setzt den Rahmenstil in C++."
type: docs
weight: 7000
url: /de/cpp/aspose.words/border/get_linestyle/
---
## Border::get_LineStyle method


Liefert oder setzt den Rahmenstil.

```cpp
Aspose::Words::LineStyle Aspose::Words::Border::get_LineStyle()
```

## Hinweise


Wenn Sie den Linienstil auf none setzen, wird die Linienbreite automatisch auf null geändert.

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

* Enum [LineStyle](../../linestyle/)
* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
