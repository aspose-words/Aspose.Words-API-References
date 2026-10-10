---
title: "Aspose::Words::Saving::ImageSaveOptions::get_SaveFormat metod"
linktitle: "get_SaveFormat"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::ImageSaveOptions::get_SaveFormat metod. Anger det format i vilket de renderade dokumentsidorna eller formerna kommer att sparas om detta spara‑alternativ‑objekt används. Kan vara ett raster‑Tiff, Png, Bmp, Jpeg eller ett vektor‑Emf, Eps, WebP, Svg i C++."
type: docs
weight: 13000
url: /sv/cpp/aspose.words.saving/imagesaveoptions/get_saveformat/
---
## ImageSaveOptions::get_SaveFormat method


Anger det format i vilket de renderade dokumentsidorna eller formerna kommer att sparas om detta spara‑alternativ‑objekt används. Kan vara ett raster [Tiff](../../../aspose.words/saveformat/), [Png](../../../aspose.words/saveformat/), [Bmp](../../../aspose.words/saveformat/), [Jpeg](../../../aspose.words/saveformat/) eller ett vektor [Emf](../../../aspose.words/saveformat/), [Eps](../../../aspose.words/saveformat/), [WebP](../), [Svg](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::ImageSaveOptions::get_SaveFormat() override
```

## Anmärkningar


Antalet andra alternativ beror på det valda formatet.

Det är också möjligt att spara till SVG både via [ImageSaveOptions](../) och via [SvgSaveOptions](../../svgsaveoptions/).

## Exempel



Visar hur man redigerar bilden medan Aspose.Words konverterar ett dokument till en sådan.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// När vi sparar dokumentet som en bild kan vi skicka ett SaveOptions‑objekt till
// redigera bilden medan sparningsoperationen renderar den.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
// Vi kan justera dessa egenskaper för att ändra bildens ljusstyrka och kontrast.
// Båda är på en 0‑1 skala och har standardvärdet 0,5.
options->set_ImageBrightness(0.3f);
options->set_ImageContrast(0.7f);
// Vi kan justera horisontell och vertikal upplösning med dessa egenskaper.
// Detta kommer att påverka bildens dimensioner.
// Standardvärdet för dessa egenskaper är 96,0, för en upplösning på 96 dpi.
options->set_HorizontalResolution(72.f);
options->set_VerticalResolution(72.f);
// Vi kan skala bilden med denna egenskap. Standardvärdet är 1,0, för en skalning på 100 %.
// Vi kan använda denna egenskap för att motverka eventuella förändringar i bildens dimensioner som en förändring av upplösningen skulle orsaka.
options->set_Scale(96.f / 72.f);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.EditImage.png", options);
```

## Se även

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
