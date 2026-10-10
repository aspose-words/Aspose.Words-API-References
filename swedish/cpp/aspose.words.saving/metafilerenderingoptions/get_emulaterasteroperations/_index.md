---
title: "Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRasterOperations metod"
linktitle: "get_EmulateRasterOperations"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRasterOperations metod. Hämtar eller anger ett värde som bestämmer om rasteroperationer ska emuleras i C++ eller inte."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.saving/metafilerenderingoptions/get_emulaterasteroperations/
---
## MetafileRenderingOptions::get_EmulateRasterOperations method


Hämtar eller anger ett värde som bestämmer om rasteroperationer ska emuleras eller inte.

```cpp
bool Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRasterOperations() const
```

## Anmärkningar


Specifika rasteroperationer kan användas i metafiler. De kan inte renderas direkt till vektorgrafik. Emulering av rasteroperationer kräver partiell rasterisering av den resulterande vektorgrafiken, vilket kan påverka metafilens renderingsprestanda.

När detta värde är satt till **true**, emulerar Aspose.Words rasteroperationerna. Det resulterande resultatet kan bli delvis rasteriserat och prestandan kan bli långsammare.

När detta värde är satt till **false**, emulerar inte Aspose.Words rasteroperationerna. När [Aspose.Words](../../../aspose.words/) stöter på en rasteroperation i en metafil återgår den till att rendera metafilen till en bitmap genom att använda operativsystemet.

Detta alternativ används endast när metafilen renderas som vektorgrafik.

Standardvärdet är **true**.
## Se även

* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
