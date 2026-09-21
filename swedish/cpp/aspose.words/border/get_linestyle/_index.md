---
title: "Aspose::Words::Border::get_LineStyle metod"
linktitle: "get_LineStyle"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Border::get_LineStyle metod. Hämtar eller anger kantstilen i C++."
type: docs
weight: 7000
url: /sv/cpp/aspose.words/border/get_linestyle/
---
## Border::get_LineStyle method


Hämtar eller anger kantstilen.

```cpp
Aspose::Words::LineStyle Aspose::Words::Border::get_LineStyle()
```

## Anmärkningar


Om du sätter linjestilen till none ändras linjebredden automatiskt till noll.

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

* Enum [LineStyle](../../linestyle/)
* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
