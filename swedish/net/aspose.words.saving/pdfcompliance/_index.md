---
title: PdfCompliance Enum
linktitle: PdfCompliance
articleTitle: PdfCompliance
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Saving.PdfCompliance enum för att förbättra din PDF-standardefterlevnad. Förbättra dokumentkvaliteten med skräddarsydda alternativ för alla behov!
type: docs
weight: 6200
url: /sv/net/aspose.words.saving/pdfcompliance/
---
## PdfCompliance enumeration

Anger efterlevnadsnivån för PDF-standarder.

```csharp
public enum PdfCompliance
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Pdf17 | `0` | Utdatafilen kommer att följa PDF 1.7-standarden (ISO 32000-1). |
| Pdf20 | `1` | Utdatafilen kommer att följa PDF 2.0-standarden (ISO 32000-2). |
| PdfA1a | `2` | Utdatafilen ska följa standarden PDF/A-1a (ISO 19005-1). Denna nivå inkluderar alla krav i PDF/A-1b och kräver dessutom att dokumentstrukturen inkluderas (även känd som "taggad"), med syftet att säkerställa att dokumentinnehållet kan sökas och återanvändas. |
| PdfA1b | `3` | Utdatafilen kommer att följa standarden PDF/A-1b (ISO 19005-1). PDF/A-1b har som mål att säkerställa tillförlitlig reproduktion av dokumentets visuella utseende. |
| PdfA2a | `4` | Utdatafilen ska följa PDF/A-2a-standarden (ISO 19005-2). Denna nivå inkluderar alla krav i PDF/A-2u och kräver dessutom att dokumentstrukturen inkluderas (även känd som "taggad"), med syftet att säkerställa att dokumentinnehållet kan sökas och återanvändas. |
| PdfA2u | `5` | Utdatafilen kommer att följa PDF/A-2u-standarden (ISO 19005-2). PDF/A-2u har som mål att bevara dokumentets statiska visuella utseende över tid, oberoende av de verktyg och system som används för att skapa, lagra eller rendera filerna. Dessutom kan all text i dokumentet extraheras på ett tillförlitligt sätt som en serie Unicode-kodpunkter. |
| PdfA3a | `6` | Utdatafilen ska följa standarden PDF/A-3a (ISO 19005-3). Denna nivå inkluderar alla krav i PDF/A-3u och kräver dessutom att dokumentstrukturen inkluderas (även känd som "taggad"), med syftet att säkerställa att dokumentinnehållet kan sökas och återanvändas. |
| PdfA3u | `7` | Utdatafilen kommer att följa PDF/A-3u-standarden (ISO 19005-3). PDF/A-3u (liksom PDF/A-2u) har som mål att bevara dokumentets statiska visuella utseende över tid, oberoende av de verktyg och system som används för att skapa, lagra eller rendera filerna. Dessutom kan all text i dokumentet extraheras på ett tillförlitligt sätt som en serie Unicode-kodpunkter. Förutom PDF/A-2u tillåter PDF/A-3u inbäddning av bilagor till PDF-dokumentet. |
| PdfA4 | `8` | Utdatafilen kommer att följa PDF/A-4-standarden (ISO 19005-4:2020). PDF/A-4 har som mål att bevara dokumentets statiska visuella utseende över tid, oberoende av de verktyg och system som används för att skapa, lagra eller rendera filerna. Dessutom kan all text i dokumentet extraheras på ett tillförlitligt sätt som en serie Unicode-kodpunkter. |
| PdfA4f | `9` | Utdatafilen kommer att följa standarden PDF/A-4f (ISO 19005-4:2020). Denna nivå inkluderar alla krav för PDF/A-4 och tillåter dessutom inbäddning av bilagor till PDF-dokumentet. |
| PdfA4Ua2 | `10` | Utdatafilen kommer att följa både PDF/A-4 (ISO 19005-4:2020) och PDF/UA-2 (ISO 14289-2:2024) standarder. PDF/A-4 har som mål att bevara dokumentets statiska visuella utseende över tid, oberoende av de verktyg och system som används för att skapa, lagra eller rendera filerna. Det primära syftet med PDF/UA är att definiera hur elektroniska dokument ska representeras i PDF-format på ett sätt som gör att filen är tillgänglig. |
| PdfUa1 | `11` | Utdatafilen kommer att följa standarden PDF/UA-1 (ISO 14289-1). Det primära syftet med PDF/UA är att definiera hur elektroniska dokument ska representeras i PDF-format på ett sätt som gör att filen är tillgänglig. |
| PdfUa2 | `12` | Utdatafilen ska följa standarden PDF/UA-2 (ISO 14289-2:2024). Det primära syftet med PDF/UA är att definiera hur elektroniska dokument ska representeras i PDF-format på ett sätt som gör att filen är tillgänglig. |

## Exempel

Visar hur man ställer in PDF-standardefterlevnadsnivån för sparade PDF-dokument.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
// Observera att vissa PdfSaveOptions är förbjudna när man sparar enligt en av standarderna och åtgärdas automatiskt.
// Använd IWarningCallback för att veta vilka alternativ som åtgärdas automatiskt.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Ställ in egenskapen "Compliance" till "PdfCompliance.PdfA1b" för att följa standarden "PDF/A-1b",
// som syftar till att bevara dokumentets visuella utseende eftersom Aspose.Words konverterar det till PDF.
// Ställ in egenskapen "Compliance" till "PdfCompliance.Pdf17" för att följa standarden "1.7".
// Ställ in egenskapen "Compliance" till "PdfCompliance.PdfA1a" för att följa standarden "PDF/A-1a",
// som följer "PDF/A-1b" samt bevarar originaldokumentets dokumentstruktur.
// Ställ in egenskapen "Compliance" till "PdfCompliance.PdfUa1" för att följa standarden "PDF/UA-1" (ISO 14289-1),
// som syftar till att definiera representation av elektroniska dokument i PDF som gör att filen är tillgänglig.
// Ställ in egenskapen "Compliance" till "PdfCompliance.Pdf20" för att följa standarden "PDF 2.0" (ISO 32000-2).
// Ställ in egenskapen "Compliance" till "PdfCompliance.PdfA4" för att följa standarden "PDF/A-4" (ISO 19004:2020),
// som bevarar dokumentets statiska visuella utseende över tid.
// Ställ in egenskapen "Compliance" till "PdfCompliance.PdfA4Ua2" för att följa både PDF/A-4 (ISO 19005-4:2020)
// och PDF/UA-2 (ISO 14289-2:2024) standarder.
// Ställ in egenskapen "Compliance" till "PdfCompliance.PdfUa2" för att följa PDF/UA-2-standarden (ISO 14289-2:2024).
// Detta hjälper till att göra dokument sökbara men kan avsevärt öka storleken på redan stora dokument.
saveOptions.Compliance = pdfCompliance;

doc.Save(ArtifactsDir + "PdfSaveOptions.Compliance.pdf", saveOptions);
```

### Se även

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
