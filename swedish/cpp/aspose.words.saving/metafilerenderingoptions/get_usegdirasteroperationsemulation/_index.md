---
title: "Aspose::Words::Saving::MetafileRenderingOptions::get_UseGdiRasterOperationsEmulation metod"
linktitle: "get_UseGdiRasterOperationsEmulation"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::MetafileRenderingOptions::get_UseGdiRasterOperationsEmulation metod. Hämtar eller anger ett värde som bestämmer om GDI+ ska användas för emulering av rasteroperationer i C++."
type: docs
weight: 8000
url: /sv/cpp/aspose.words.saving/metafilerenderingoptions/get_usegdirasteroperationsemulation/
---
## MetafileRenderingOptions::get_UseGdiRasterOperationsEmulation method


Hämtar eller anger ett värde som bestämmer om GDI+ ska användas för emulering av rasteroperationer eller inte.

```cpp
bool Aspose::Words::Saving::MetafileRenderingOptions::get_UseGdiRasterOperationsEmulation() const
```

## Anmärkningar


Windows GDI+-biblioteket kan användas för att emulera rasteroperationer. Det ger stöd för alla rasteroperationer jämfört med Aspose.Words egen emulering, men prestandan kan vara långsammare i vissa fall.

När detta värde är satt till **true**, använder Aspose.Words GDI+ för emulering av rasteroperationer.

När detta värde är satt till **false**, använder Aspose.Words sin egen implementation av emulering av rasteroperationer.

Detta alternativ används endast när metafilen renderas som vektorgrafik.

Standardvärdet är **false**.

## Exempel



Visar hur man ställer in renderingsläget när man sparar dokument med Windows‑Metafile‑bilder till andra bildformat.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertImage(get_ImageDir() + u"Windows MetaFile.wmf");

// När vi sparar dokumentet som en bild kan vi skicka ett SaveOptions‑objekt till
// bestämmer hur sparningsoperationen kommer att behandla Windows‑Metafiler i dokumentet.
// Om vi sätter egenskapen "RenderingMode" till "MetafileRenderingMode.Vector",
// eller "MetafileRenderingMode.VectorWithFallback", kommer vi att rendera alla metafiler som vektorgrafik.
// Om vi sätter egenskapen "RenderingMode" till "MetafileRenderingMode.Bitmap", kommer vi att rendera alla metafiler som bitmapbilder.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
options->get_MetafileRenderingOptions()->set_RenderingMode(metafileRenderingMode);
// Aspose.Words använder GDI+ för emulering av rasteroperationer när värdet är satt till true.
options->get_MetafileRenderingOptions()->set_UseGdiRasterOperationsEmulation(true);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.WindowsMetaFile.png", options);
```

## Se även

* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
