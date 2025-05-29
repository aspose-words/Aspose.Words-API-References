---
title: MailMerger.ExecuteWithRegionsToImages
linktitle: ExecuteWithRegionsToImages
articleTitle: ExecuteWithRegionsToImages
second_title: Aspose.Words für .NET
description: Fügen Sie mit MailMerger ExecuteWithRegionsToImages mühelos Daten aus einer DataTable in Dokumente ein und verwandeln Sie Ihre Inhalte in beeindruckende Bilder.
type: docs
weight: 50
url: /de/net/aspose.words.lowcode/mailmerger/executewithregionstoimages/
---
## ExecuteWithRegionsToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregionstoimages_3}

Führt einen Serienbrief aus einer DataTable in das Dokument mit Serienbriefbereichen aus und rendert das Ergebnis in Bilder.

```csharp
public static Stream[] ExecuteWithRegionsToImages(string inputFileName, 
    ImageSaveOptions saveOptions, DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| saveOptions | ImageSaveOptions | Die Speicheroptionen der Ausgabe. |
| dataTable | DataTable | Tabelle mit Daten, die in Seriendruckfelder eingefügt werden sollen. Bei Feldnamen wird die Groß- und Kleinschreibung nicht berücksichtigt. Ein im Dokument nicht gefundener Feldname wird ignoriert. |
| mailMergeOptions | MailMergeOptions | Optionen für Serienbriefe. |

## Beispiele

Zeigt, wie Sie aus einer Datentabelle einen Serienbrief mit Regionenoperationen erstellen und das Ergebnis in Bildern speichern.

```csharp
// Es gibt mehrere Möglichkeiten, Serienbriefe mit Regionen aus einer DataTable heraus zu erstellen:
string doc = MyDir + "Mail merge with regions.docx";

DataTable dataTable = new DataTable("MyTable");
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("LastName");
dataTable.Rows.Add(new object[] { "John", "Doe" });
dataTable.Rows.Add(new object[] { "", "" });
dataTable.Rows.Add(new object[] { "Jane", "Doe" });

Stream[] images = MailMerger.ExecuteWithRegionsToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataTable);
images = MailMerger.ExecuteWithRegionsToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataTable, new MailMergeOptions() { TrimWhitespaces = true });
```

### Siehe auch

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## ExecuteWithRegionsToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregionstoimages_1}

Führt einen Serienbrief aus einer DataTable in das Dokument mit Serienbriefbereichen aus und rendert das Ergebnis in Bilder.

```csharp
public static Stream[] ExecuteWithRegionsToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | Stream | Der Eingabedateistream. |
| saveOptions | ImageSaveOptions | Die Speicheroptionen der Ausgabe. |
| dataTable | DataTable | Tabelle mit Daten, die in Seriendruckfelder eingefügt werden sollen. Bei Feldnamen wird die Groß- und Kleinschreibung nicht berücksichtigt. Ein im Dokument nicht gefundener Feldname wird ignoriert. |
| mailMergeOptions | MailMergeOptions | Optionen für Serienbriefe. |

## Beispiele

Zeigt, wie Sie aus einer DataTable unter Verwendung von Dokumenten aus dem Stream einen Serienbrief mit Regionen-Operation ausführen und das Ergebnis in Bildern speichern.

```csharp
// Es gibt mehrere Möglichkeiten, Serienbriefe mit Regionen aus einer DataTable unter Verwendung von Dokumenten aus dem Stream auszuführen:
DataTable dataTable = new DataTable("MyTable");
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("LastName");
dataTable.Rows.Add(new object[] { "John", "Doe" });
dataTable.Rows.Add(new object[] { "", "" });
dataTable.Rows.Add(new object[] { "Jane", "Doe" });

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    Stream[] images = MailMerger.ExecuteWithRegionsToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), dataTable);
    images = MailMerger.ExecuteWithRegionsToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), dataTable, new MailMergeOptions() { TrimWhitespaces = true });
}
```

### Siehe auch

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## ExecuteWithRegionsToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataSet, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregionstoimages_2}

Führt einen Serienbrief aus einem DataSet in das Dokument mit Serienbriefbereichen aus und rendert das Ergebnis in Bilder.

```csharp
public static Stream[] ExecuteWithRegionsToImages(string inputFileName, 
    ImageSaveOptions saveOptions, DataSet dataSet, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| saveOptions | ImageSaveOptions | Die Speicheroptionen der Ausgabe. |
| dataSet | DataSet | DataSet, das Daten enthält, die in Serienbrieffelder eingefügt werden sollen. |
| mailMergeOptions | MailMergeOptions | Optionen für Serienbriefe. |

## Beispiele

Zeigt, wie Sie aus einem DataSet einen Serienbrief mit Regionenoperationen erstellen und das Ergebnis in Bildern speichern.

```csharp
// Es gibt mehrere Möglichkeiten, Serienbriefe mit Regionen aus einem DataSet heraus durchzuführen:
string doc = MyDir + "Mail merge with regions data set.docx";

DataTable tableCustomers = new DataTable("Customers");
tableCustomers.Columns.Add("CustomerID");
tableCustomers.Columns.Add("CustomerName");
tableCustomers.Rows.Add(new object[] { 1, "John Doe" });
tableCustomers.Rows.Add(new object[] { 2, "Jane Doe" });

DataTable tableOrders = new DataTable("Orders");
tableOrders.Columns.Add("CustomerID");
tableOrders.Columns.Add("ItemName");
tableOrders.Columns.Add("Quantity");
tableOrders.Rows.Add(new object[] { 1, "Hawaiian", 2 });
tableOrders.Rows.Add(new object[] { 2, "Pepperoni", 1 });
tableOrders.Rows.Add(new object[] { 2, "Chicago", 1 });

DataSet dataSet = new DataSet();
dataSet.Tables.Add(tableCustomers);
dataSet.Tables.Add(tableOrders);
dataSet.Relations.Add(tableCustomers.Columns["CustomerID"], tableOrders.Columns["CustomerID"]);

Stream[] images = MailMerger.ExecuteWithRegionsToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataSet);
images = MailMerger.ExecuteWithRegionsToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataSet, new MailMergeOptions() { TrimWhitespaces = true });
```

### Siehe auch

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## ExecuteWithRegionsToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataSet, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregionstoimages}

Führt einen Serienbrief aus einem DataSet in das Dokument mit Serienbriefbereichen aus und rendert das Ergebnis in Bilder.

```csharp
public static Stream[] ExecuteWithRegionsToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    DataSet dataSet, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | Stream | Der Eingabedateistream. |
| saveOptions | ImageSaveOptions | Die Speicheroptionen der Ausgabe. |
| dataSet | DataSet | DataSet, das Daten enthält, die in Serienbrieffelder eingefügt werden sollen. |
| mailMergeOptions | MailMergeOptions | Optionen für Serienbriefe. |

## Beispiele

Zeigt, wie Sie aus einem DataSet unter Verwendung von Dokumenten aus dem Stream einen Serienbrief mit Regionen-Operation durchführen und das Ergebnis in Bildern speichern.

```csharp
// Es gibt mehrere Möglichkeiten, Serienbriefe mit Regionen aus einem DataSet unter Verwendung von Dokumenten aus dem Stream auszuführen:
DataTable tableCustomers = new DataTable("Customers");
tableCustomers.Columns.Add("CustomerID");
tableCustomers.Columns.Add("CustomerName");
tableCustomers.Rows.Add(new object[] { 1, "John Doe" });
tableCustomers.Rows.Add(new object[] { 2, "Jane Doe" });

DataTable tableOrders = new DataTable("Orders");
tableOrders.Columns.Add("CustomerID");
tableOrders.Columns.Add("ItemName");
tableOrders.Columns.Add("Quantity");
tableOrders.Rows.Add(new object[] { 1, "Hawaiian", 2 });
tableOrders.Rows.Add(new object[] { 2, "Pepperoni", 1 });
tableOrders.Rows.Add(new object[] { 2, "Chicago", 1 });

DataSet dataSet = new DataSet();
dataSet.Tables.Add(tableCustomers);
dataSet.Tables.Add(tableOrders);
dataSet.Relations.Add(tableCustomers.Columns["CustomerID"], tableOrders.Columns["CustomerID"]);

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    Stream[] images = MailMerger.ExecuteWithRegionsToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), dataSet);
    images = MailMerger.ExecuteWithRegionsToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), dataSet, new MailMergeOptions() { TrimWhitespaces = true });
}
```

### Siehe auch

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)
