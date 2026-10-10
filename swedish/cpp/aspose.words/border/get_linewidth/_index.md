---
title: "Aspose::Words::Border::get_LineWidth‑metod"
linktitle: "get_LineWidth"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Border::get_LineWidth‑metod. Hämtar eller anger kantens bredd i punkter i C++."
type: docs
weight: 8000
url: /sv/cpp/aspose.words/border/get_linewidth/
---
## Border::get_LineWidth method


Hämtar eller anger kantbredden i punkter.

```cpp
double Aspose::Words::Border::get_LineWidth()
```

## Anmärkningar


Om du anger en linjebredd större än noll när linjestilen är ingen, ändras linjestilen automatiskt till enkel linje.

## Exempel



Visar hur man infogar en sträng omgiven av en kant i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->get_Border()->set_Color(System::Drawing::Color::get_Green());
builder->get_Font()->get_Border()->set_LineWidth(2.5);
builder->get_Font()->get_Border()->set_LineStyle(Aspose::Words::LineStyle::DashDotStroker);

builder->Write(u"Text surrounded by green border.");

doc->Save(get_ArtifactsDir() + u"Border.FontBorder.docx");
```

## Se även

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
