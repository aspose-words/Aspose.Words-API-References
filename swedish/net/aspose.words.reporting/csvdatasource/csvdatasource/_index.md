---
title: CsvDataSource
linktitle: CsvDataSource
articleTitle: CsvDataSource
second_title: Aspose.Words för .NET
description: Skapa enkelt en kraftfull CSV-datakälla med vår CsvDataSource-konstruktor. Förenkla dataparsning med standardalternativ för sömlös integration.
type: docs
weight: 10
url: /sv/net/aspose.words.reporting/csvdatasource/csvdatasource/
---
## CsvDataSource(*string*) {#constructor_2}

Skapar en ny datakälla med data från en CSV-fil med standardalternativ för att analysera CSV-data.

```csharp
public CsvDataSource(string csvPath)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| csvPath | String | Sökvägen till CSV-filen som ska användas som datakälla. |

### Se även

* class [CsvDataSource](../)
* namnutrymme [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* hopsättning [Aspose.Words](../../../)

---

## CsvDataSource(*string, [CsvDataLoadOptions](../../csvdataloadoptions/)*) {#constructor_3}

Skapar en ny datakälla med data från en CSV-fil med hjälp av de angivna alternativen för att analysera CSV-data.

```csharp
public CsvDataSource(string csvPath, CsvDataLoadOptions options)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| csvPath | String | Sökvägen till CSV-filen som ska användas som datakälla. |
| options | CsvDataLoadOptions | Alternativ för att analysera CSV-data. |

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

* class [CsvDataLoadOptions](../../csvdataloadoptions/)
* class [CsvDataSource](../)
* namnutrymme [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* hopsättning [Aspose.Words](../../../)

---

## CsvDataSource(*Stream*) {#constructor}

Skapar en ny datakälla med data från en CSV-ström med standardalternativ för att analysera CSV-data.

```csharp
public CsvDataSource(Stream csvStream)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| csvStream | Stream | Den CSV-dataström som ska användas som datakälla. |

### Se även

* class [CsvDataSource](../)
* namnutrymme [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* hopsättning [Aspose.Words](../../../)

---

## CsvDataSource(*Stream, [CsvDataLoadOptions](../../csvdataloadoptions/)*) {#constructor_1}

Skapar en ny datakälla med data från en CSV-ström med hjälp av de angivna alternativen för att analysera CSV-data.

```csharp
public CsvDataSource(Stream csvStream, CsvDataLoadOptions options)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| csvStream | Stream | Den CSV-dataström som ska användas som datakälla. |
| options | CsvDataLoadOptions | Alternativ för att analysera CSV-data. |

## Exempel

Visar hur man använder CSV som datakälla (ström).

```csharp
Document doc = new Document(MyDir + "Reporting engine template - CSV data destination.docx");

CsvDataLoadOptions loadOptions = new CsvDataLoadOptions(true);
loadOptions.Delimiter = ';';
loadOptions.CommentChar = '$';

using (FileStream stream = File.OpenRead(MyDir + "List of people.csv"))
{
    CsvDataSource dataSource = new CsvDataSource(stream, loadOptions);
    BuildReport(doc, dataSource, "persons");
}

doc.Save(ArtifactsDir + "ReportingEngine.CsvDataStream.docx");
```

### Se även

* class [CsvDataLoadOptions](../../csvdataloadoptions/)
* class [CsvDataSource](../)
* namnutrymme [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* hopsättning [Aspose.Words](../../../)
