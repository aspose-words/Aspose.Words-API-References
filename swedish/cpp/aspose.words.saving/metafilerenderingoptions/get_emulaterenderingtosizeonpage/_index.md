---
title: "Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRenderingToSizeOnPage metod"
linktitle: "get_EmulateRenderingToSizeOnPage"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRenderingToSizeOnPage metod. Hämtar eller anger ett värde som bestämmer om metafilrenderingen emulerar visningen av metafilen enligt storleken på sidan eller visningen av metafilen i dess standardstorlek i C++."
type: docs
weight: 4334
url: /sv/cpp/aspose.words.saving/metafilerenderingoptions/get_emulaterenderingtosizeonpage/
---
## MetafileRenderingOptions::get_EmulateRenderingToSizeOnPage method


Hämtar eller anger ett värde som bestämmer om metafilrendering emulerar visningen av metafilen enligt sidans storlek eller i dess standardstorlek.

```cpp
bool Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRenderingToSizeOnPage() const
```

## Anmärkningar


När metafiler visas i MS Word kan vissa grafik skalas enligt den faktiska metafilstorleken i pixlar. Dvs. även zoomning kan påverka metafilens visning.

När detta värde är inställt på **true**, Aspose.Words emulerar rendering enligt metafilens storlek på sidan. Storleken i pixlar beräknas från metafilens storlek på sidan och den angivna [EmulateRenderingToSizeOnPageResolution](../get_emulaterenderingtosizeonpageresolution/).

När detta värde är inställt på **false**, emulerar Aspose.Words metafilrendering till dess standardstorlek i pixlar.

Detta alternativ används endast när metafilen renderas som vektorgrafik.

Standardvärdet är **true**.
## Se även

* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
