---
title: "Aspose::Words::Saving::PdfSaveOptions::get_FontEmbeddingMode‑metod"
linktitle: "get_FontEmbeddingMode"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::PdfSaveOptions::get_FontEmbeddingMode‑metod. Anger teckensnittsinbäddningsläget i C++."
type: docs
weight: 18000
url: /sv/cpp/aspose.words.saving/pdfsaveoptions/get_fontembeddingmode/
---
## PdfSaveOptions::get_FontEmbeddingMode method


Anger teckensnittsinbäddningsläget.

```cpp
Aspose::Words::Saving::PdfFontEmbeddingMode Aspose::Words::Saving::PdfSaveOptions::get_FontEmbeddingMode() const
```

## Anmärkningar


Standardvärdet är [EmbedAll](../../pdffontembeddingmode/).

Denna inställning fungerar endast för text i ANSI‑kodning (Windows‑1252). Om dokumentet innehåller icke‑ANSI‑text kommer motsvarande teckensnitt att bäddas in oavsett denna inställning.

PDF/A‑ och PDF/UA‑efterlevnad kräver att alla teckensnitt bäddas in. Värdet [EmbedAll](../../pdffontembeddingmode/) kommer att användas automatiskt vid sparande till PDF/A och PDF/UA.
## Se även

* Enum [PdfFontEmbeddingMode](../../pdffontembeddingmode/)
* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
