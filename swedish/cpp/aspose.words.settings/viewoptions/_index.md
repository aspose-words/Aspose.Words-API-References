---
title: "Aspose::Words::Settings::ViewOptions class"
linktitle: "ViewOptions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Settings::ViewOptions class. Tillhandahåller olika alternativ som styr hur ett dokument visas i Microsoft Word. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 9000
url: /sv/cpp/aspose.words.settings/viewoptions/
---
## ViewOptions class


Tillhandahåller olika alternativ som styr hur ett dokument visas i Microsoft Word. För att lära dig mer, besök dokumentationsartikeln [Work with Options and Appearance of Word Documents](https://docs.aspose.com/words/cpp/work-with-word-document-options-and-appearance/).

```cpp
class ViewOptions : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_DisplayBackgroundShape](./get_displaybackgroundshape/)() const | Styr visning av bakgrundsformen i utskriftslayoutvy. |
| [get_DoNotDisplayPageBoundaries](./get_donotdisplaypageboundaries/)() const | Stänger av visning av utrymmet mellan textens överkant och sidans övre kant. |
| [get_FormsDesign](./get_formsdesign/)() const | Anger om dokumentet är i formulärdesignläge. |
| [get_ViewType](./get_viewtype/)() const | Styr visningsläget i Microsoft Word. |
| [get_ZoomPercent](./get_zoompercent/)() const | Hämtar eller anger den procentandel du vill visa ditt dokument i. |
| [get_ZoomType](./get_zoomtype/)() const | Hämtar eller anger ett zoomvärde baserat på fönstrets storlek. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DisplayBackgroundShape](./set_displaybackgroundshape/)(bool) | Sättare för [Aspose::Words::Settings::ViewOptions::get_DisplayBackgroundShape](./get_displaybackgroundshape/). |
| [set_DoNotDisplayPageBoundaries](./set_donotdisplaypageboundaries/)(bool) | Sättare för [Aspose::Words::Settings::ViewOptions::get_DoNotDisplayPageBoundaries](./get_donotdisplaypageboundaries/). |
| [set_FormsDesign](./set_formsdesign/)(bool) | Sättare för [Aspose::Words::Settings::ViewOptions::get_FormsDesign](./get_formsdesign/). |
| [set_ViewType](./set_viewtype/)(Aspose::Words::Settings::ViewType) | Sättare för [Aspose::Words::Settings::ViewOptions::get_ViewType](./get_viewtype/). |
| [set_ZoomPercent](./set_zoompercent/)(int32_t) | Sättare för [Aspose::Words::Settings::ViewOptions::get_ZoomPercent](./get_zoompercent/). |
| [set_ZoomType](./set_zoomtype/)(Aspose::Words::Settings::ZoomType) | Inställare för [Aspose::Words::Settings::ViewOptions::get_ZoomType](./get_zoomtype/). |
| static [Type](./type/)() |  |

## Exempel



Visar hur man ställer in en anpassad zoomfaktor, som äldre versioner av Microsoft Word kommer att tillämpa på ett dokument vid inläsning.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

doc->get_ViewOptions()->set_ViewType(Aspose::Words::Settings::ViewType::PageLayout);
doc->get_ViewOptions()->set_ZoomPercent(50);

ASSERT_EQ(Aspose::Words::Settings::ZoomType::Custom, doc->get_ViewOptions()->get_ZoomType());
ASSERT_EQ(Aspose::Words::Settings::ZoomType::None, doc->get_ViewOptions()->get_ZoomType());

doc->Save(get_ArtifactsDir() + u"ViewOptions.SetZoomPercentage.doc");
```


Visar hur man ställer in en anpassad zoomtyp, som äldre versioner av Microsoft Word kommer att tillämpa på ett dokument vid inläsning.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Ställ in egenskapen "ZoomType" till "ZoomType.PageWidth" för att få Microsoft Word
// för att automatiskt zooma dokumentet så att det passar sidans bredd.
// Ställ in egenskapen "ZoomType" till "ZoomType.FullPage" för att få Microsoft Word
// för att automatiskt zooma dokumentet så att hela första sidan blir synlig.
// Ställ in egenskapen "ZoomType" till "ZoomType.TextFit" för att få Microsoft Word
// för att automatiskt zooma dokumentet så att det passar de inre textmarginalerna på första sidan.
doc->get_ViewOptions()->set_ZoomType(zoomType);

doc->Save(get_ArtifactsDir() + u"ViewOptions.SetZoomType.doc");
```

## Se även

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
