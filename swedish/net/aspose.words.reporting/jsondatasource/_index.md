---
title: JsonDataSource Class
linktitle: JsonDataSource
articleTitle: JsonDataSource
second_title: Aspose.Words för .NET
description: Aspose.Words.Reporting.JsonDataSource klass. Ger tillgång till data för en JSONfil eller ström som ska användas i en rapport i C#.
type: docs
weight: 4690
url: /sv/net/aspose.words.reporting/jsondatasource/
---
## JsonDataSource class

Ger tillgång till data för en JSON-fil eller ström som ska användas i en rapport.

För att lära dig mer, besök[LINQ Reporting Engine](https://docs.aspose.com/words/net/linq-reporting-engine/) dokumentationsartikel.

```csharp
public class JsonDataSource
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [JsonDataSource](jsondatasource/#constructor)(*Stream*) | Skapar en ny datakälla med data från en JSON-ström med standardalternativ för att tolka JSON-data. |
| [JsonDataSource](jsondatasource/#constructor_2)(*string*) | Skapar en ny datakälla med data från en JSON-fil med standardalternativ för att tolka JSON-data. |
| [JsonDataSource](jsondatasource/#constructor_1)(*Stream, [JsonDataLoadOptions](../jsondataloadoptions/)*) | Skapar en ny datakälla med data från en JSON-ström med de angivna alternativen för att analysera JSON-data. |
| [JsonDataSource](jsondatasource/#constructor_3)(*string, [JsonDataLoadOptions](../jsondataloadoptions/)*) | Skapar en ny datakälla med data från en JSON-fil med de angivna alternativen för att tolka JSON-data. |

## Anmärkningar

För att komma åt data för motsvarande fil eller ström medan du genererar en rapport, skicka en instans av den här klassen as en datakälla till en av[`ReportingEngine`](../reportingengine/) .BuildReport overloads.

I malldokument, om ett JSON-element på toppnivå är en array,`JsonDataSource` instans bör behandlas på samma sätt som om det vore enDataTable instans. Om ett JSON-element på toppnivå är ett objekt, en`JsonDataSource` instans bör behandlas på samma sätt som om det vore aDataRow instans. För mer information, se mallsyntaxreferens (https://docs.aspose.com/display/wordsnet/Template+Syntax).

I malldokument kan du arbeta med inskrivna värden för JSON-element. För enkelhetens skull ersätter motorn uppsättningen av JSON enkla typer med följande:

* Nullable
* Nullable
* Nullable
* Nullable
* String

Motorn känner automatiskt igen värden för de extra typerna på deras JSON-representationer.

För att åsidosätta standardbeteendet för JSON-dataladdning, initiera och skicka ett[`JsonDataLoadOptions`](../jsondataloadoptions/) instans till en konstruktor av denna klass.

### Se även

* namnutrymme [Aspose.Words.Reporting](../../aspose.words.reporting/)
* hopsättning [Aspose.Words](../../)
