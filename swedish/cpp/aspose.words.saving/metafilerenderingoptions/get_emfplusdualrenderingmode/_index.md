---
title: "Aspose::Words::Saving::MetafileRenderingOptions::get_EmfPlusDualRenderingMode metod"
linktitle: "get_EmfPlusDualRenderingMode"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::MetafileRenderingOptions::get_EmfPlusDualRenderingMode metod. Hämtar eller anger ett värde som bestämmer hur EMF+ Dual-metafiler ska renderas i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.saving/metafilerenderingoptions/get_emfplusdualrenderingmode/
---
## MetafileRenderingOptions::get_EmfPlusDualRenderingMode method


Hämtar eller anger ett värde som bestämmer hur EMF+ Dual-metafiler ska renderas.

```cpp
Aspose::Words::Saving::EmfPlusDualRenderingMode Aspose::Words::Saving::MetafileRenderingOptions::get_EmfPlusDualRenderingMode() const
```

## Anmärkningar


EMF+ Dual-metafiler innehåller både EMF+ och EMF-delar. MS Word och GDI+ renderar alltid EMF+-delen. Aspose.Words stöder för närvarande inte fullt ut alla EMF+-poster och i vissa fall ser renderingsresultatet av EMF-delen bättre ut än renderingsresultatet av EMF+-delen.

Detta alternativ används endast när metafilen renderas som vektorgrafik. När metafilen renderas till en bitmap används EMF+-delen alltid.

Standardvärdet är [EmfPlusWithFallback](../../emfplusdualrenderingmode/).
## Se även

* Enum [EmfPlusDualRenderingMode](../../emfplusdualrenderingmode/)
* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
