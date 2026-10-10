---
title: "Aspose::Words::Border::get_Color-Methode"
linktitle: "get_Color"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Border::get_Color-Methode. Liest oder setzt die Rahmenfarbe in C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words/border/get_color/
---
## Border::get_Color method


Liefert oder setzt die Rahmenfarbe.

```cpp
System::Drawing::Color Aspose::Words::Border::get_Color()
```


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
