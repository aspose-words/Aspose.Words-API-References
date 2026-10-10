---
title: "Aspose::Words::Saving::ImageSaveOptions::get_MetafileRenderingOptions‑metoden"
linktitle: "get_MetafileRenderingOptions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::ImageSaveOptions::get_MetafileRenderingOptions‑metoden. Tillåter att ange hur metafiler behandlas i den renderade utdata i C++."
type: docs
weight: 9000
url: /sv/cpp/aspose.words.saving/imagesaveoptions/get_metafilerenderingoptions/
---
## ImageSaveOptions::get_MetafileRenderingOptions method


Tillåter att ange hur metafiler behandlas i den renderade utdata.

```cpp
System::SharedPtr<Aspose::Words::Saving::MetafileRenderingOptions> Aspose::Words::Saving::ImageSaveOptions::get_MetafileRenderingOptions()
```

## Anmärkningar


När [Vector](../../metafilerenderingmode/) anges, renderar Aspose.Words metafilen till vektorgrafik med sin egen metafil‑renderingsmotor först och renderar sedan vektorgrafiken till bilden.

När [Bitmap](../../metafilerenderingmode/) anges, renderar Aspose.Words metafilen direkt till bilden med GDI+‑metafil‑renderingsmotorn.

GDI+‑metafil‑renderingsmotorn fungerar snabbare, stödjer nästan alla metafil‑funktioner men kan vid låga upplösningar ge inkonsekventa resultat jämfört med resten av vektorgrafiken (särskilt för text) på sidan. Aspose.Words‑metafil‑renderingsmotorn ger mer konsekventa resultat även vid låga upplösningar men är långsammare och kan återge komplexa metafiler felaktigt.

Standardvärdet för [MetafileRenderingMode](../../metafilerenderingmode/) är [Bitmap](../../metafilerenderingmode/).

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

* Class [MetafileRenderingOptions](../../metafilerenderingoptions/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
