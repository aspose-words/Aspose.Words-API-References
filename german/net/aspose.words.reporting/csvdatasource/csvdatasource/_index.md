---
title: CsvDataSource
linktitle: CsvDataSource
articleTitle: CsvDataSource
second_title: Aspose.Words für .NET
description: Erstellen Sie mühelos eine leistungsstarke CSV-Datenquelle mit unserem CsvDataSource-Konstruktor. Vereinfachen Sie die Datenanalyse mit Standardoptionen für eine nahtlose Integration.
type: docs
weight: 10
url: /de/net/aspose.words.reporting/csvdatasource/csvdatasource/
---
## CsvDataSource(*string*) {#constructor_2}

Erstellt eine neue Datenquelle mit Daten aus einer CSV-Datei unter Verwendung der Standardoptionen zum Parsen von CSV-Daten.

```csharp
public CsvDataSource(string csvPath)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| csvPath | String | Der Pfad zur CSV-Datei, die als Datenquelle verwendet werden soll. |

### Siehe auch

* class [CsvDataSource](../)
* namensraum [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Montage [Aspose.Words](../../../)

---

## CsvDataSource(*string, [CsvDataLoadOptions](../../csvdataloadoptions/)*) {#constructor_3}

Erstellt eine neue Datenquelle mit Daten aus einer CSV-Datei unter Verwendung der angegebenen Optionen zum Parsen von CSV-Daten.

```csharp
public CsvDataSource(string csvPath, CsvDataLoadOptions options)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| csvPath | String | Der Pfad zur CSV-Datei, die als Datenquelle verwendet werden soll. |
| options | CsvDataLoadOptions | Optionen zum Parsen der CSV-Daten. |

## Beispiele

Zeigt, wie CSV als Datenquelle (Zeichenfolge) verwendet wird.

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

### Siehe auch

* class [CsvDataLoadOptions](../../csvdataloadoptions/)
* class [CsvDataSource](../)
* namensraum [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Montage [Aspose.Words](../../../)

---

## CsvDataSource(*Stream*) {#constructor}

Erstellt eine neue Datenquelle mit Daten aus einem CSV-Stream unter Verwendung der Standardoptionen zum Parsen von CSV-Daten.

```csharp
public CsvDataSource(Stream csvStream)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| csvStream | Stream | Der CSV-Datenstrom, der als Datenquelle verwendet werden soll. |

### Siehe auch

* class [CsvDataSource](../)
* namensraum [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Montage [Aspose.Words](../../../)

---

## CsvDataSource(*Stream, [CsvDataLoadOptions](../../csvdataloadoptions/)*) {#constructor_1}

Erstellt eine neue Datenquelle mit Daten aus einem CSV-Stream unter Verwendung der angegebenen Optionen zum Parsen von CSV-Daten.

```csharp
public CsvDataSource(Stream csvStream, CsvDataLoadOptions options)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| csvStream | Stream | Der CSV-Datenstrom, der als Datenquelle verwendet werden soll. |
| options | CsvDataLoadOptions | Optionen zum Parsen der CSV-Daten. |

## Beispiele

Zeigt, wie CSV als Datenquelle (Stream) verwendet wird.

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

### Siehe auch

* class [CsvDataLoadOptions](../../csvdataloadoptions/)
* class [CsvDataSource](../)
* namensraum [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Montage [Aspose.Words](../../../)
