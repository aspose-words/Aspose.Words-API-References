---
title: CsvDataSource Class
linktitle: CsvDataSource
articleTitle: CsvDataSource
second_title: Aspose.Words för .NET
description: Få tillgång till och använd CSV-data utan problem med Aspose.Words.Reporting.CsvDataSource. Förbättra dina rapporter med sömlös dataintegration!
type: docs
weight: 5410
url: /sv/net/aspose.words.reporting/csvdatasource/
---
## CsvDataSource class

Ger åtkomst till data från en CSV-fil eller ström som ska användas i en rapport.

För att lära dig mer, besök[LINQ-rapporteringsmotor](https://docs.aspose.com/words/net/linq-reporting-engine/) dokumentationsartikel.

```csharp
public class CsvDataSource
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [CsvDataSource](csvdatasource/#constructor)(*Stream*) | Skapar en ny datakälla med data från en CSV-ström med standardalternativ för att analysera CSV-data. |
| [CsvDataSource](csvdatasource/#constructor_2)(*string*) | Skapar en ny datakälla med data från en CSV-fil med standardalternativ för att analysera CSV-data. |
| [CsvDataSource](csvdatasource/#constructor_1)(*Stream, [CsvDataLoadOptions](../csvdataloadoptions/)*) | Skapar en ny datakälla med data från en CSV-ström med hjälp av de angivna alternativen för att analysera CSV-data. |
| [CsvDataSource](csvdatasource/#constructor_3)(*string, [CsvDataLoadOptions](../csvdataloadoptions/)*) | Skapar en ny datakälla med data från en CSV-fil med hjälp av de angivna alternativen för att analysera CSV-data. |

## Anmärkningar

För att komma åt data i motsvarande fil eller ström när du genererar en rapport, skicka en instans av denna klass som en datakälla till en av[`ReportingEngine`](../reportingengine/) .BuildReport överbelastningar.

I malldokument, en`CsvDataSource` instansen bör behandlas på samma sätt som om den vore aDataTable -instansen. För mer information, se mallsyntaxreferensen (https://docs.aspose.com/display/wordsnet/Template+Syntax).

Datatyper med kommaseparerade värden bestäms automatiskt utifrån deras strängrepresentationer. Så i malldokument kan du arbeta med typade värden snarare än bara strängar. Motorn kan automatiskt känna igen värden av följande typer:

* Nullable
* Nullable
* Nullable
* Nullable
* String

Observera att för att automatisk igenkänning av datatyper ska fungera bör strängrepresentationer av kommaseparerade värden bildas med hjälp av invarianta kulturinställningar.

För att åsidosätta standardbeteendet för CSV-datainläsning, initiera och skicka en[`CsvDataLoadOptions`](../csvdataloadoptions/) instance till en konstruktor av denna klass.

## Exempel

Visar hur man använder CSV som datakälla (sträng).

```csharp
Document doc = new Document(MyDir + "Reporting engine template - CSV data destination.docx");

CsvDataLoadOptions loadOptions = new CsvDataLoadOptions(true);
loadOptions.Delimiter = ';';
loadOptions.CommentChar = '$';
loadOptions.HasHeaders = true;
loadOptions.QuoteChar = '"';

CsvDataSource dataSource = new CsvDataSource(MyDir + "List of people.csv", loadOptions);
BuildReport(doc, dataSource, "persons");

doc.Save(ArtifactsDir + "ReportingEngine.CsvDataString.docx");
```

### Se även

* namnutrymme [Aspose.Words.Reporting](../../aspose.words.reporting/)
* hopsättning [Aspose.Words](../../)
