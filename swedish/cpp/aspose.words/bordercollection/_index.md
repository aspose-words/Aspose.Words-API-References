---
title: "Aspose::Words::BorderCollection klass"
linktitle: "BorderCollection"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::BorderCollection klass. En samling av Border-objekt. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 8000
url: /sv/cpp/aspose.words/bordercollection/
---
## BorderCollection class


En samling av [Border](../border/) objekt. För att lära dig mer, besök dokumentationsartikeln [Programmering med dokument](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class BorderCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Border>>
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Tar bort alla kanter på ett objekt. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::BorderCollection\>\&) | Jämför samlingar av kanter. |
| [get_Bottom](./get_bottom/)() | Hämtar den nedre kanten. |
| [get_Color](./get_color/)() | Hämtar eller anger kantens färg. |
| [get_Count](./get_count/)() | Hämtar antalet kanter i samlingen. |
| [get_DistanceFromText](./get_distancefromtext/)() | Hämtar eller anger avståndet för kanten från texten i punkter. |
| [get_Horizontal](./get_horizontal/)() | Hämtar den horisontella kanten som används mellan celler eller motsvarande stycken. |
| [get_Left](./get_left/)() | Hämtar den vänstra kanten. |
| [get_LineStyle](./get_linestyle/)() | Hämtar eller anger kantstilen. |
| [get_LineWidth](./get_linewidth/)() | Hämtar eller anger kantbredden i punkter. |
| [get_Right](./get_right/)() | Hämtar den högra kanten. |
| [get_Shadow](./get_shadow/)() | Hämtar eller anger ett värde som indikerar om kanten har en skugga. |
| [get_Top](./get_top/)() | Hämtar den övre kanten. |
| [get_Vertical](./get_vertical/)() | Hämtar den vertikala kanten som används mellan celler. |
| [GetEnumerator](./getenumerator/)() override | Returnerar ett enumeratorobjekt som kan användas för att iterera över alla kanter i samlingen. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(Aspose::Words::BorderType) | Hämtar ett [Border](../border/) objekt efter kanttyp. |
| [idx_get](./idx_get/)(int32_t) | Hämtar ett [Border](../border/) objekt efter index. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Color](./set_color/)(System::Drawing::Color) | Sättare för [Aspose::Words::BorderCollection::get_Color](./get_color/). |
| [set_DistanceFromText](./set_distancefromtext/)(double) | Sättare för [Aspose::Words::BorderCollection::get_DistanceFromText](./get_distancefromtext/). |
| [set_LineStyle](./set_linestyle/)(Aspose::Words::LineStyle) | Sättare för [Aspose::Words::BorderCollection::get_LineStyle](./get_linestyle/). |
| [set_LineWidth](./set_linewidth/)(double) | Sättare för [Aspose::Words::BorderCollection::get_LineWidth](./get_linewidth/). |
| [set_Shadow](./set_shadow/)(bool) | Sättare för [Aspose::Words::BorderCollection::get_Shadow](./get_shadow/). |
| static [Type](./type/)() |  |

## Exempel



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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
