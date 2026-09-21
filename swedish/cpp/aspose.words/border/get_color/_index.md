---
title: "Aspose::Words::Border::get_Color‑metod"
linktitle: "get_Color"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Border::get_Color‑metod. Hämtar eller anger kantens färg i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words/border/get_color/
---
## Border::get_Color method


Hämtar eller anger kantens färg.

```cpp
System::Drawing::Color Aspose::Words::Border::get_Color()
```


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
