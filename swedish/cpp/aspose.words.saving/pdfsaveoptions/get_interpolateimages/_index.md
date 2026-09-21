---
title: "Aspose::Words::Saving::PdfSaveOptions::get_InterpolateImages metod"
linktitle: "get_InterpolateImages"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::PdfSaveOptions::get_InterpolateImages metod. En flagga som indikerar om bildinterpolering ska utföras av en kompatibel läsare. När false anges skrivs inte flaggan till utdatafilen och läsarens standardbeteende används istället i C++."
type: docs
weight: 22000
url: /sv/cpp/aspose.words.saving/pdfsaveoptions/get_interpolateimages/
---
## PdfSaveOptions::get_InterpolateImages method


En flagga som indikerar om bildinterpolering ska utföras av en kompatibel läsare. När **false** anges skrivs inte flaggan till utdatafilen och läsarens standardbeteende används istället.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_InterpolateImages() const
```

## Anmärkningar


När upplösningen på en källbild är betydligt lägre än den för utmatningsenheten täcker varje källprov många enhetspixlar. Som ett resultat kan bilder framstå som hackiga eller blockiga. Dessa visuella artefakter kan minskas genom att tillämpa en bildinterpoleringsalgoritm under rendering. Istället för att måla alla pixlar som täcks av ett källprov med samma färg försöker bildinterpolering skapa en mjuk övergång mellan intilliggande provvärden.

En kompatibel Reader kan välja att inte implementera denna PDF‑funktion, eller kan använda någon specifik implementation av interpolering som den önskar.

Standardvärdet är **false**.

Interpoleringsflaggan är förbjuden enligt PDF/A‑kompatibilitet. **false**‑värdet kommer att användas automatiskt vid sparande till PDF/A.
## Se även

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
