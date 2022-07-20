---
title: JsonDataSource
second_title: Aspose.Words för .NET API Referens
description: Ger tillgång till data för en JSON-fil eller ström som ska användas i en rapport.
type: docs
weight: 4430
url: /sv/net/aspose.words.reporting/jsondatasource/
---
## JsonDataSource class

Ger tillgång till data för en JSON-fil eller ström som ska användas i en rapport.

```csharp
public class JsonDataSource
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [JsonDataSource](jsondatasource#constructor)(Stream) | Skapar en ny datakälla med data från en JSON-ström med standardalternativ för att tolka JSON-data. |
| [JsonDataSource](jsondatasource#constructor_2)(string) | Skapar en ny datakälla med data från en JSON-fil med standardalternativ för att tolka JSON-data. |
| [JsonDataSource](jsondatasource#constructor_1)(Stream, JsonDataLoadOptions) | Skapar en ny datakälla med data från en JSON-ström med de angivna alternativen för att analysera JSON-data. |
| [JsonDataSource](jsondatasource#constructor_3)(string, JsonDataLoadOptions) | Skapar en ny datakälla med data från en JSON-fil med de angivna alternativen för att tolka JSON-data. |

### Anmärkningar

För att komma åt data för motsvarande fil eller ström medan du genererar en rapport, skicka en instans av den här klassen as en datakälla till en av[`ReportingEngine`](../reportingengine) .BuildReport overloads.

I malldokument, om ett JSON-element på toppnivå är en array,[`JsonDataSource`](../jsondatasource) instans bör behandlas på samma sätt som om det vore enDataTable instans. Om ett JSON-element på toppnivå är ett objekt, en[`JsonDataSource`](../jsondatasource) instans bör behandlas på samma sätt som om det vore aDataRow instans. För mer information, se mallsyntaxreferens (https://docs.aspose.com/display/wordsnet/Template+Syntax).

I malldokument kan du arbeta med inskrivna värden för JSON-element. För enkelhetens skull ersätter motorn uppsättningen av JSON enkla typer med följande:

* Nullable
* Nullable
* Nullable
* Nullable
* String

Motorn känner automatiskt igen värden för de extra typerna på deras JSON-representationer.

För att åsidosätta standardbeteendet för JSON-dataladdning, initiera och skicka ett[`JsonDataLoadOptions`](../jsondataloadoptions)instans till en konstruktor av denna klass.

### Se även

* namnutrymme [Aspose.Words.Reporting](../../aspose.words.reporting)
* hopsättning [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->