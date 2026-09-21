---
title: "Aspose::Words::Saving::PdfSaveOptions::get_UseCoreFonts metod"
linktitle: "get_UseCoreFonts"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::PdfSaveOptions::get_UseCoreFonts metod. Hämtar eller anger ett värde som bestämmer om TrueType‑typsnitten Arial, Times New Roman, Courier New och Symbol ska ersättas med kärn‑PDF Type 1‑typsnitt i C++."
type: docs
weight: 32000
url: /sv/cpp/aspose.words.saving/pdfsaveoptions/get_usecorefonts/
---
## PdfSaveOptions::get_UseCoreFonts method


Hämtar eller anger ett värde som bestämmer om TrueType‑typsnitten Arial, Times New Roman, Courier New och Symbol ska ersättas med PDF:s kärn‑Type 1‑typsnitt eller inte.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_UseCoreFonts() const
```

## Anmärkningar


Standardvärdet är **false**. När detta värde sätts till **true** ersätts typsnitten Arial, Times New Roman, Courier New och Symbol i PDF‑dokumentet med motsvarande kärn‑Type 1‑typsnitt.

Kärn‑PDF‑typsnitt, eller deras teckensnittsmått och lämpliga ersättningstypsnitt, måste vara tillgängliga för alla PDF‑visningsprogram.

Denna inställning fungerar endast för text i ANSI (Windows‑1252)‑kodning. Icke‑ANSI‑text kommer att skrivas med inbäddat TrueType‑typsnitt oavsett denna inställning.

PDF/A- och PDF/UA-efterlevnad kräver att alla teckensnitt bäddas in. **false** värdet kommer att användas automatiskt vid sparande till PDF/A och PDF/UA.

Kärnteckensnitt stöds inte vid sparande till PDF 2.0-format. **false** värdet kommer att användas automatiskt vid sparande till PDF 2.0.

Detta alternativ har högre prioritet än alternativet [FontEmbeddingMode](../get_fontembeddingmode/).
## Se även

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
