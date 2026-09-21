---
title: "Aspose::Words::Saving::MultiPageLayout class"
linktitle: "MultiPageLayout"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::MultiPageLayout-klass. Definierar en layout för att rendera flera sidor till en enda utdata i C++."
type: docs
weight: 14500
url: /sv/cpp/aspose.words.saving/multipagelayout/
---
## MultiPageLayout class


Definierar en layout för att rendera flera sidor till en enda utdata.

```cpp
class MultiPageLayout : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_BackColor](./get_backcolor/)() | Hämtar bakgrundsfärgen för utdata. Standardvärdet är **Empty**. |
| [get_BorderColor](./get_bordercolor/)() | Hämtar färgen på sidornas kant. Standardvärdet är **Empty**. |
| [get_BorderWidth](./get_borderwidth/)() const | Hämtar bredden på sidornas kant. Standardvärdet är 0. |
| [GetType](./gettype/)() const override |  |
| static [Grid](./grid/)(int32_t, float, float) | Skapar en layout där sidor renderas från vänster till höger, uppifrån och ner, i ett rutnät med det angivna antalet kolumner. |
| static [Horizontal](./horizontal/)(float) | Skapar en layout där alla angivna sidor renderas horisontellt sida vid sida, från vänster till höger, i en enda utdata. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_BackColor](./set_backcolor/)(System::Drawing::Color) | Ställer in bakgrundsfärgen för utdata. Standardvärdet är **Empty**. |
| [set_BorderColor](./set_bordercolor/)(System::Drawing::Color) | Ställer in färgen på sidornas kant. Standardvärdet är **Empty**. |
| [set_BorderWidth](./set_borderwidth/)(float) | Ställer in bredden på sidornas kant. Standardvärdet är 0. |
| static [SinglePage](./singlepage/)() | Skapar en layout som renderar endast den första av de angivna sidorna. |
| static [TiffFrames](./tiffframes/)() | Skapar en layout där varje sida renderas som en separat ram i en multi-ram TIFF-bild. Gäller endast TIFF-bildformat. |
| static [Type](./type/)() |  |
| static [Vertical](./vertical/)(float) | Skapar en layout där alla angivna sidor renderas vertikalt, en under den andra, i en enda utdata. |

## Exempel



Visar hur man sparar dokumentet som en JPG-bild med inställningar för flersidig layout.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// Ställ in en rutnätslayout med:
// - 3 kolumner per rad.
// - 10pt avstånd mellan sidor (horisontellt och vertikalt).
options->set_PageLayout(Aspose::Words::Saving::MultiPageLayout::Grid(3, 10.0f, 10.0f));

// Alternativa layouter:
// options.PageLayout = MultiPageLayout.Horizontal(10);
// options.PageLayout = MultiPageLayout.Vertical(10);

// Anpassa bakgrunden och kanten.
options->get_PageLayout()->set_BackColor(System::Drawing::Color::get_LightGray());
options->get_PageLayout()->set_BorderColor(System::Drawing::Color::get_Blue());
options->get_PageLayout()->set_BorderWidth(2.0f);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.GridLayout.jpg", options);
```

## Se även

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
