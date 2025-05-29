---
title: JsonDataSource Class
linktitle: JsonDataSource
articleTitle: JsonDataSource
second_title: Aspose.Words för .NET
description: Lås upp kraftfull rapportering med Aspose.Words.Reporting.JsonDataSource. Få enkel åtkomst till JSON-data för sömlös integration i dina rapporter.
type: docs
weight: 5430
url: /sv/net/aspose.words.reporting/jsondatasource/
---
## JsonDataSource class

Ger åtkomst till data från en JSON-fil eller ström som ska användas i en rapport.

För att lära dig mer, besök[LINQ-rapporteringsmotor](https://docs.aspose.com/words/net/linq-reporting-engine/) dokumentationsartikel.

```csharp
public class JsonDataSource
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [JsonDataSource](jsondatasource/#constructor)(*Stream*) | Skapar en ny datakälla med data från en JSON-ström med standardalternativ för att analysera JSON-data. |
| [JsonDataSource](jsondatasource/#constructor_2)(*string*) | Skapar en ny datakälla med data från en JSON-fil med standardalternativ för att analysera JSON-data. |
| [JsonDataSource](jsondatasource/#constructor_1)(*Stream, [JsonDataLoadOptions](../jsondataloadoptions/)*) | Skapar en ny datakälla med data från en JSON-ström med hjälp av de angivna alternativen för att analysera JSON-data. |
| [JsonDataSource](jsondatasource/#constructor_3)(*string, [JsonDataLoadOptions](../jsondataloadoptions/)*) | Skapar en ny datakälla med data från en JSON-fil med hjälp av de angivna alternativen för att analysera JSON-data. |

## Anmärkningar

För att komma åt data i motsvarande fil eller ström när du genererar en rapport, skicka en instans av denna klass som en datakälla till en av[`ReportingEngine`](../reportingengine/) .BuildReport överbelastningar.

I malldokument, om ett JSON-element på toppnivå är en array, en`JsonDataSource` instansen bör behandlas på samma sätt som om den vore enDataTable -instans. Om ett JSON-element på toppnivå är ett objekt, en`JsonDataSource` instansen bör behandlas på samma sätt som om den vore aDataRow -instansen. För mer information, se mallsyntaxreferensen (https://docs.aspose.com/display/wordsnet/Template+Syntax).

I malldokument kan du arbeta med typade värden för JSON-element. För enkelhetens skull ersätter motorn mängden av enkla JSON-typer med följande:

* Nullable
* Nullable
* Nullable
* Nullable
* String

Motorn känner automatiskt igen värden för de extra typerna baserat på deras JSON-representationer.

För att åsidosätta standardbeteendet för JSON-datainläsning, initiera och skicka en[`JsonDataLoadOptions`](../jsondataloadoptions/) instance till en konstruktor av denna klass.

## Exempel

Visar hur man använder JSON som datakälla (sträng).

```csharp
Document doc = new Document(MyDir + "Reporting engine template - JSON data destination.docx");

JsonDataLoadOptions options = new JsonDataLoadOptions
{
    ExactDateTimeParseFormats = new List<string> {"MM/dd/yyyy", "MM.d.yy", "MM d yy"},
    AlwaysGenerateRootObject = true,
    PreserveSpaces = true,
    SimpleValueParseMode = JsonSimpleValueParseMode.Loose
};

JsonDataSource dataSource = new JsonDataSource(MyDir + "List of people.json", options);
BuildReport(doc, dataSource, "persons");

doc.Save(ArtifactsDir + "ReportingEngine.JsonDataString.docx");
```

### Se även

* namnutrymme [Aspose.Words.Reporting](../../aspose.words.reporting/)
* hopsättning [Aspose.Words](../../)
