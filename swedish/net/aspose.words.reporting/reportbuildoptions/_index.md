---
title: ReportBuildOptions Enum
linktitle: ReportBuildOptions
articleTitle: ReportBuildOptions
second_title: Aspose.Words för .NET
description: Upptäck alternativen i Aspose.Words ReportingEngine för effektiv rapportgenerering. Anpassa din rapportering med flexibla inställningar för optimala resultat.
type: docs
weight: 5460
url: /sv/net/aspose.words.reporting/reportbuildoptions/
---
## ReportBuildOptions enumeration

Anger alternativ som styr beteendet för[`ReportingEngine`](../reportingengine/) medan man skapar en rapport.

```csharp
[Flags]
public enum ReportBuildOptions
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `0` | Anger standardalternativ. |
| AllowMissingMembers | `1` | Anger att saknade objektmedlemmar ska behandlas som null-literaler av motorn. Det här alternativet påverkar endast åtkomst till instansobjektmedlemmar (det vill säga icke-statiska) och tilläggsmetoder. Om det här -alternativet inte är angivet genererar motorn ett undantag när den stöter på en saknad objektmedlem. |
| RemoveEmptyParagraphs | `2` | Anger att sökmotorn ska ta bort stycken som blir tomma efter att mallsyntaxtaggar har tagits bort eller ersatts med tomma värden. |
| InlineErrorMessages | `4` | Anger att motorn ska infoga felmeddelanden från mallsyntax i utdatadokument. Om det här alternativet inte är angivet genererar motorn ett undantag när den stöter på ett syntaxfel. |
| UseLegacyHeaderFooterVisiting | `8` | Anger att sökmotorn ska besöka underordnade sektionsnoder (sidhuvuden, sidfötter, brödtexter) i en ordning som är kompatibel med Aspose.Words-versioner tidigare än 21.9. |
| RespectJpegExifOrientation | `10` | Anger att motorn ska använda EXIF-bildorienteringsvärden för att rotera infogade JPEG-bilder på lämpligt sätt. |
| UpdateFieldsSyntaxAware | `20` | Anger att sökmotorn ska ignorera mallsyntax i fältresultat och uppdatera fält efter att en rapport har skapats. |

### Se även

* namnutrymme [Aspose.Words.Reporting](../../aspose.words.reporting/)
* hopsättning [Aspose.Words](../../)
