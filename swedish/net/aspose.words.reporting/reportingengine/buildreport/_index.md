---
title: BuildReport
second_title: Aspose.Words för .NET API Referens
description: Fyller i det angivna malldokumentet med data från den angivna källan vilket gör det till en klar rapport.
type: docs
weight: 40
url: /sv/net/aspose.words.reporting/reportingengine/buildreport/
---
## BuildReport(Document, object) {#buildreport}

Fyller i det angivna malldokumentet med data från den angivna källan vilket gör det till en klar rapport.

```csharp
public bool BuildReport(Document document, object dataSource)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| document | Document | Ett malldokument som ska fyllas i med data. |
| dataSource | Object | Ett datakällaobjekt. |

### Returvärde

En flagga som indikerar om analysen av malldokumentet lyckades. Den returnerade flaggan är bara meningsfull om ett värde på[`Options`](../options/)egenskapen inkluderar InlineErrorMessages alternativ.

### Anmärkningar

Med denna överbelastning kan du referera till datakällans medlemmar i malldokumentet, men du kan inte referera till själva datakällans objekt. Du bör använda`BuildReport` överbelastning för att uppnå detta.

Ett datakällobjekt kan vara av en av följande typer:

* [`XmlDataSource`](../../xmldatasource/)
* [`JsonDataSource`](../../jsondatasource/)
* [`CsvDataSource`](../../csvdatasource/)
* DataSet
* DataTable
* DataRow
* IDataReader
* IDataRecord
* DataView
* DataRowView
* Alla andra godtyckliga icke-dynamiska och icke-anonyma .NET type

För information om hur man arbetar med datakällor av olika typer i malldokument, se mallsyntax referens (https://docs.aspose.com/display/wordsnet/Template+Syntax).

### Se även

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* namnutrymme [Aspose.Words.Reporting](../../reportingengine/)
* hopsättning [Aspose.Words](../../../)

---

## BuildReport(Document, object, string) {#buildreport_1}

Fyller i det angivna malldokumentet med data från den angivna källan vilket gör det till en klar rapport.

```csharp
public bool BuildReport(Document document, object dataSource, string dataSourceName)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| document | Document | Ett malldokument som ska fyllas i med data. |
| dataSource | Object | Ett datakällaobjekt. |
| dataSourceName | String | Ett namn som refererar till datakällobjektet i mallen. |

### Returvärde

En flagga som indikerar om analysen av malldokumentet lyckades. Den returnerade flaggan är bara meningsfull om ett värde på[`Options`](../options/)egenskapen inkluderar InlineErrorMessages alternativ.

### Anmärkningar

Med denna överbelastning kan du referera till datakällans medlemmar och själva datakällans objekt i mallen. Om du inte ska referera till själva datakällobjektet kan du utelämna*dataSourceName* passerar null eller använd`BuildReport` överbelastning.

Ett datakällobjekt kan vara av en av följande typer:

* [`XmlDataSource`](../../xmldatasource/)
* [`JsonDataSource`](../../jsondatasource/)
* [`CsvDataSource`](../../csvdatasource/)
* DataSet
* DataTable
* DataRow
* IDataReader
* IDataRecord
* DataView
* DataRowView
* Alla andra godtyckliga icke-dynamiska och icke-anonyma .NET type

För information om hur man arbetar med datakällor av olika typer i malldokument, se mallsyntax referens (https://docs.aspose.com/display/wordsnet/Template+Syntax).

### Se även

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* namnutrymme [Aspose.Words.Reporting](../../reportingengine/)
* hopsättning [Aspose.Words](../../../)

---

## BuildReport(Document, object[], string[]) {#buildreport_2}

Fyller i det angivna malldokumentet med data från de angivna källorna vilket gör det till en klar rapport.

```csharp
public bool BuildReport(Document document, object[] dataSources, string[] dataSourceNames)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| document | Document | Ett malldokument som ska fyllas i med data. |
| dataSources | Object[] | En uppsättning datakällobjekt. |
| dataSourceNames | String[] | En uppsättning namn för att referera till datakällobjekten i mallen. |

### Returvärde

En flagga som indikerar om analysen av malldokumentet lyckades. Den returnerade flaggan är bara meningsfull om ett värde på[`Options`](../options/)egenskapen inkluderar InlineErrorMessages alternativ.

### Anmärkningar

Genom att använda denna överbelastning kan du referera till flera datakällobjekt och deras medlemmar i mallen. Namnet på den första datakällan kan utelämnas (dvs. vara en tom sträng eller null) om du ska referera till datakällans medlemmar men inte själva datakällans objekt. Namnen på de andra datakällorna måste anges och vara unika.

Om du ska använda en enda datakälla, överväg att använda av`BuildReport` och`BuildReport` överbelastning istället.

Ett datakällobjekt kan vara av en av följande typer:

* [`XmlDataSource`](../../xmldatasource/)
* [`JsonDataSource`](../../jsondatasource/)
* [`CsvDataSource`](../../csvdatasource/)
* DataSet
* DataTable
* DataRow
* IDataReader
* IDataRecord
* DataView
* DataRowView
* Alla andra godtyckliga icke-dynamiska och icke-anonyma .NET type

För information om hur man arbetar med datakällor av olika typer i malldokument, se mallsyntax referens (https://docs.aspose.com/display/wordsnet/Template+Syntax).

### Se även

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* namnutrymme [Aspose.Words.Reporting](../../reportingengine/)
* hopsättning [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
