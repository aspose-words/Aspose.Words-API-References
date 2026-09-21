---
title: "Aspose::Words::Border class"
linktitle: "Border"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Border class. Representerar en kant av ett objekt. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 7000
url: /sv/cpp/aspose.words/border/
---
## Border class


Representerar en kant på ett objekt. För att läsa mer, besök dokumentationsartikeln [Programmering med dokument](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class Border : public Aspose::Words::InternableComplexAttr,
               public Aspose::Words::IComplexAttr
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Återställer kantegenskaper till standardvärden. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Border\>\&) | Bestämmer om den angivna kanten är lika i värde med den aktuella kanten. |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Bestämmer om det angivna objektet är lika i värde med det aktuella objektet. |
| [get_Color](./get_color/)() | Hämtar eller anger kantens färg. |
| [get_DistanceFromText](./get_distancefromtext/)() | Hämtar eller anger avståndet för kanten från texten eller från sidans kant i punkter. |
| [get_IsVisible](./get_isvisible/)() | Returnerar **true** om [LineStyle](./get_linestyle/) inte är [None](../linestyle/). |
| [get_LineStyle](./get_linestyle/)() | Hämtar eller anger kantstilen. |
| [get_LineWidth](./get_linewidth/)() | Hämtar eller anger kantbredden i punkter. |
| [get_Shadow](./get_shadow/)() | Hämtar eller anger ett värde som indikerar om kanten har en skugga. |
| [get_ThemeColor](./get_themecolor/)() | Hämtar eller anger temafärgen i det tillämpade färgschemat som är associerat med detta [Border](./) objekt. |
| [get_TintAndShade](./get_tintandshade/)() | Hämtar eller anger ett dubbelvärde som ljusar upp eller mörkar en färg. |
| [GetHashCode](./gethashcode/)() const override | Fungerar som en hash-funktion för denna typ. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Color](./set_color/)(System::Drawing::Color) | Sättare för [Aspose::Words::Border::get_Color](./get_color/). |
| [set_DistanceFromText](./set_distancefromtext/)(double) | Sättare för [Aspose::Words::Border::get_DistanceFromText](./get_distancefromtext/). |
| [set_LineStyle](./set_linestyle/)(Aspose::Words::LineStyle) | Inställningsmetod för [Aspose::Words::Border::get_LineStyle](./get_linestyle/). |
| [set_LineWidth](./set_linewidth/)(double) | Inställningsmetod för [Aspose::Words::Border::get_LineWidth](./get_linewidth/). |
| [set_Shadow](./set_shadow/)(bool) | Inställningsmetod för [Aspose::Words::Border::get_Shadow](./get_shadow/). |
| [set_ThemeColor](./set_themecolor/)(Aspose::Words::Themes::ThemeColor) | Inställningsmetod för [Aspose::Words::Border::get_ThemeColor](./get_themecolor/). |
| [set_TintAndShade](./set_tintandshade/)(double) | Inställningsmetod för [Aspose::Words::Border::get_TintAndShade](./get_tintandshade/). |
| static [Type](./type/)() |  |
## Anmärkningar


Kanter kan tillämpas på olika dokumentelement, inklusive stycke, textsekvens i ett stycke eller en tabellcell.

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


Visar hur man infogar ett stycke med en övre kant.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Border> topBorder = builder->get_ParagraphFormat()->get_Borders()->get_Top();
topBorder->set_LineWidth(4.0);
topBorder->set_LineStyle(Aspose::Words::LineStyle::DashSmallGap);
// Ställ in ThemeColor endast när LineWidth eller LineStyle har satts.
topBorder->set_ThemeColor(Aspose::Words::Themes::ThemeColor::Accent1);
topBorder->set_TintAndShade(0.25);

builder->Writeln(u"Text with a top border.");

doc->Save(get_ArtifactsDir() + u"Border.ParagraphTopBorder.docx");
```

## Se även

* Class [InternableComplexAttr](../internablecomplexattr/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
