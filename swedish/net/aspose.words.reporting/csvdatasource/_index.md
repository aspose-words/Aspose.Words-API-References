---
title: Class CsvDataSource
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Reporting.CsvDataSource klass. Ger tillgång till data från en CSVfil eller ström som ska användas i en rapport.
type: docs
weight: 4410
url: /sv/net/aspose.words.reporting/csvdatasource/
---
## CsvDataSource class

Ger tillgång till data från en CSV-fil eller ström som ska användas i en rapport.

```csharp
public class CsvDataSource
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [CsvDataSource](csvdatasource/#constructor)(Stream) | Skapar en ny datakälla med data från en CSV-ström med standardalternativ för att analysera CSV-data. |
| [CsvDataSource](csvdatasource/#constructor_2)(string) | Skapar en ny datakälla med data från en CSV-fil med standardalternativ för att analysera CSV-data. |
| [CsvDataSource](csvdatasource/#constructor_1)(Stream, CsvDataLoadOptions) | Skapar en ny datakälla med data från en CSV-ström med de angivna alternativen för att analysera CSV-data. |
| [CsvDataSource](csvdatasource/#constructor_3)(string, CsvDataLoadOptions) | Skapar en ny datakälla med data från en CSV-fil med de angivna alternativen för att tolka CSV-data. |

### Anmärkningar

För att komma åt data för motsvarande fil eller ström medan du genererar en rapport, skicka en instans av den här klassen as en datakälla till en av[`ReportingEngine`](../reportingengine/) .BuildReport overloads.

I malldokument, en`CsvDataSource` instans bör behandlas på samma sätt som om den var aDataTable instans. För mer information, se mallsyntaxreferens (https://docs.aspose.com/display/wordsnet/Template+Syntax).

Datatyper av kommaseparerade värden bestäms automatiskt efter deras strängrepresentationer. Så i template -dokument kan du arbeta med inskrivna värden snarare än bara strängar. Motorn kan automatiskt känna igen värden av följande typer:

* Nullable
* Nullable
* Nullable
* Nullable
* String

Observera att för att automatisk igenkänning av datatyper ska fungera bör strängrepresentationer av kommaseparerade värden bildas med invarianta kulturinställningar.

För att åsidosätta standardbeteendet för CSV-dataladdning, initiera och skicka ett[`CsvDataLoadOptions`](../csvdataloadoptions/)instans till en konstruktor av denna klass.

### Se även

* namnutrymme [Aspose.Words.Reporting](../../aspose.words.reporting/)
* hopsättning [Aspose.Words](../../)


