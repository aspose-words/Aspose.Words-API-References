---
title: "Aspose::Words::Saving::ImageSaveOptions::get_PageLayout metod"
linktitle: "get_PageLayout"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::ImageSaveOptions::get_PageLayout metod. Hämtar eller anger layouten som används när flera sidor renderas till ett enda utdata i C++."
type: docs
weight: 9500
url: /sv/cpp/aspose.words.saving/imagesaveoptions/get_pagelayout/
---
## ImageSaveOptions::get_PageLayout method


Hämtar eller anger layouten som används när flera sidor renderas till en enda utdata.

```cpp
System::SharedPtr<Aspose::Words::Saving::MultiPageLayout> Aspose::Words::Saving::ImageSaveOptions::get_PageLayout() const
```

## Anmärkningar


Använd en av fabrikmetoderna i [MultiPageLayout](../../multipagelayout/) för att konfigurera denna egenskap.

För [Tiff](../../../aspose.words/saveformat/) är standardvärdet [TiffFrames](../../multipagelayout/tiffframes/). För andra format är standardvärdet [SinglePage](../../multipagelayout/singlepage/).

Denna egenskap har effekt endast vid sparande till följande format: [Jpeg](../../../aspose.words/saveformat/), [Gif](../../../aspose.words/saveformat/), [Png](../../../aspose.words/saveformat/), [Bmp](../../../aspose.words/saveformat/), [Tiff](../../../aspose.words/saveformat/), [WebP](../)

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

* Class [MultiPageLayout](../../multipagelayout/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
