---
title: "Aspose::Words::Saving::MetafileRenderingOptions::get_UseEmfEmbeddedToWmf metod"
linktitle: "get_UseEmfEmbeddedToWmf"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::MetafileRenderingOptions::get_UseEmfEmbeddedToWmf metod. Hämtar eller anger ett värde som bestämmer hur WMF-metafiler med inbäddade EMF-metafiler ska renderas i C++."
type: docs
weight: 7000
url: /sv/cpp/aspose.words.saving/metafilerenderingoptions/get_useemfembeddedtowmf/
---
## MetafileRenderingOptions::get_UseEmfEmbeddedToWmf method


Hämtar eller anger ett värde som bestämmer hur WMF-metafiler med inbäddade EMF-metafiler ska renderas.

```cpp
bool Aspose::Words::Saving::MetafileRenderingOptions::get_UseEmfEmbeddedToWmf() const
```

## Anmärkningar


WMF-metafiler kan innehålla inbäddade EMF-data. MS Word använder i de flesta fall inbäddade EMF-data. GDI+ använder alltid WMF-data.

När detta värde är satt till **true**, använder Aspose.Words inbäddade EMF-data vid rendering.

När detta värde är satt till **false**, använder Aspose.Words WMF-data vid rendering.

Detta alternativ används endast när metafilen renderas som vektorgrafik. När metafilen renderas till en bitmap används WMF-data alltid.

Standardvärdet är **true**.
## Se även

* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
