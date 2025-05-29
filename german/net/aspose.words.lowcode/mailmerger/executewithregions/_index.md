---
title: MailMerger.ExecuteWithRegions
linktitle: ExecuteWithRegions
articleTitle: ExecuteWithRegions
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihre Dokumenterstellung mit der ExecuteWithRegions-Methode von MailMerger. Fügen Sie DataTables mithilfe anpassbarer Regionen mühelos in Dokumente ein.
type: docs
weight: 40
url: /de/net/aspose.words.lowcode/mailmerger/executewithregions/
---
## ExecuteWithRegions(*string, string, DataTable*) {#executewithregions_9}

Führt einen Seriendruck aus einer DataTable in das Dokument mit Seriendruckbereichen durch.

```csharp
public static void ExecuteWithRegions(string inputFileName, string outputFileName, 
    DataTable dataTable)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| outputFileName | String | Der Name der Ausgabedatei. |
| dataTable | DataTable | Datenquelle für den Seriendruckvorgang. Die TableName-Eigenschaft der Tabelle muss festgelegt sein. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jedes Teil nach der Regel „outputFile_partIndex.extension“ zu generieren.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne TIFF-Datei mit mehreren Frames gespeichert.

## Beispiele

Zeigt, wie Sie aus einer DataTable einen Serienbrief mit Regionen-Operation erstellen.

```csharp
// Es gibt mehrere Möglichkeiten, Serienbriefe mit Regionen aus einer DataTable heraus zu erstellen:
string doc = MyDir + "Mail merge with regions.docx";

DataTable dataTable = new DataTable("MyTable");
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("LastName");
dataTable.Rows.Add(new object[] { "John", "Doe" });
dataTable.Rows.Add(new object[] { "", "" });
dataTable.Rows.Add(new object[] { "Jane", "Doe" });

MailMerger.ExecuteWithRegions(doc, ArtifactsDir + "LowCode.MailMergeWithRegionsDataTable.1.docx", dataTable);
MailMerger.ExecuteWithRegions(doc, ArtifactsDir + "LowCode.MailMergeWithRegionsDataTable.2.docx", SaveFormat.Docx, dataTable);
MailMerger.ExecuteWithRegions(doc, ArtifactsDir + "LowCode.MailMergeWithRegionsDataTable.3.docx", SaveFormat.Docx, dataTable, new MailMergeOptions() { TrimWhitespaces = true });
```

### Siehe auch

* class [MailMerger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## ExecuteWithRegions(*string, string, [SaveFormat](../../../aspose.words/saveformat/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregions_5}

Führt einen Seriendruck aus einer DataTable in das Dokument mit Seriendruckbereichen durch.

```csharp
public static void ExecuteWithRegions(string inputFileName, string outputFileName, 
    SaveFormat saveFormat, DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| outputFileName | String | Der Name der Ausgabedatei. |
| saveFormat | SaveFormat | Das Speicherformat der Ausgabe. |
| dataTable | DataTable | Tabelle mit Daten, die in Seriendruckfelder eingefügt werden sollen. Bei Feldnamen wird die Groß- und Kleinschreibung nicht berücksichtigt. Ein im Dokument nicht gefundener Feldname wird ignoriert. |
| mailMergeOptions | MailMergeOptions | Optionen für Serienbriefe. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jedes Teil nach der Regel „outputFile_partIndex.extension“ zu generieren.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne TIFF-Datei mit mehreren Frames gespeichert.

## Beispiele

Zeigt, wie Sie aus einer DataTable einen Serienbrief mit Regionen-Operation erstellen.

```csharp
// Es gibt mehrere Möglichkeiten, Serienbriefe mit Regionen aus einer DataTable heraus zu erstellen:
string doc = MyDir + "Mail merge with regions.docx";

DataTable dataTable = new DataTable("MyTable");
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("LastName");
dataTable.Rows.Add(new object[] { "John", "Doe" });
dataTable.Rows.Add(new object[] { "", "" });
dataTable.Rows.Add(new object[] { "Jane", "Doe" });

MailMerger.ExecuteWithRegions(doc, ArtifactsDir + "LowCode.MailMergeWithRegionsDataTable.1.docx", dataTable);
MailMerger.ExecuteWithRegions(doc, ArtifactsDir + "LowCode.MailMergeWithRegionsDataTable.2.docx", SaveFormat.Docx, dataTable);
MailMerger.ExecuteWithRegions(doc, ArtifactsDir + "LowCode.MailMergeWithRegionsDataTable.3.docx", SaveFormat.Docx, dataTable, new MailMergeOptions() { TrimWhitespaces = true });
```

### Siehe auch

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## ExecuteWithRegions(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregions_7}

Führt einen Seriendruck aus einer DataTable in das Dokument mit Seriendruckbereichen durch.

```csharp
public static void ExecuteWithRegions(string inputFileName, string outputFileName, 
    SaveOptions saveOptions, DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| outputFileName | String | Der Name der Ausgabedatei. |
| saveOptions | SaveOptions | Die Speicheroptionen der Ausgabe. |
| dataTable | DataTable | Tabelle mit Daten, die in Seriendruckfelder eingefügt werden sollen. Bei Feldnamen wird die Groß- und Kleinschreibung nicht berücksichtigt. Ein im Dokument nicht gefundener Feldname wird ignoriert. |
| mailMergeOptions | MailMergeOptions | Optionen für Serienbriefe. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jedes Teil nach der Regel „outputFile_partIndex.extension“ zu generieren.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne TIFF-Datei mit mehreren Frames gespeichert.

### Siehe auch

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## ExecuteWithRegions(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregions_1}

Führt einen Serienbriefvorgang für einen einzelnen Datensatz aus.

```csharp
public static void ExecuteWithRegions(Stream inputStream, Stream outputStream, 
    SaveFormat saveFormat, DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | Stream | Der Eingabedateistream. |
| outputStream | Stream | Der Ausgabedateistream. |
| saveFormat | SaveFormat | Das Speicherformat der Ausgabe. |
| dataTable | DataTable | Tabelle mit Daten, die in Seriendruckfelder eingefügt werden sollen. Bei Feldnamen wird die Groß- und Kleinschreibung nicht berücksichtigt. Ein im Dokument nicht gefundener Feldname wird ignoriert. |
| mailMergeOptions | MailMergeOptions | Optionen für Serienbriefe. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe im angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelnes TIFF mit mehreren Frames im angegebenen Stream gespeichert.

## Beispiele

Zeigt, wie Sie mithilfe von Dokumenten aus dem Stream einen Serienbrief mit Regionen-Vorgang aus einer DataTable heraus durchführen.

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
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeStreamWithRegionsDataTable.1.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.ExecuteWithRegions(streamIn, streamOut, SaveFormat.Docx, dataTable);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeStreamWithRegionsDataTable.2.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.ExecuteWithRegions(streamIn, streamOut, SaveFormat.Docx, dataTable, new MailMergeOptions() { TrimWhitespaces = true });
}
```

### Siehe auch

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## ExecuteWithRegions(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregions_3}

Führt einen Serienbriefvorgang für einen einzelnen Datensatz aus.

```csharp
public static void ExecuteWithRegions(Stream inputStream, Stream outputStream, 
    SaveOptions saveOptions, DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | Stream | Der Eingabedateistream. |
| outputStream | Stream | Der Ausgabedateistream. |
| saveOptions | SaveOptions | Die Speicheroptionen der Ausgabe. |
| dataTable | DataTable | Tabelle mit Daten, die in Seriendruckfelder eingefügt werden sollen. Bei Feldnamen wird die Groß- und Kleinschreibung nicht berücksichtigt. Ein im Dokument nicht gefundener Feldname wird ignoriert. |
| mailMergeOptions | MailMergeOptions | Optionen für Serienbriefe. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe im angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelnes TIFF mit mehreren Frames im angegebenen Stream gespeichert.

### Siehe auch

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## ExecuteWithRegions(*string, string, DataSet*) {#executewithregions_8}

Führt einen Serienbrief aus einem DataSet in ein Dokument mit Serienbriefbereichen aus.

```csharp
public static void ExecuteWithRegions(string inputFileName, string outputFileName, DataSet dataSet)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| outputFileName | String | Der Name der Ausgabedatei. |
| dataSet | DataSet | DataSet, das Daten enthält, die in Serienbrieffelder eingefügt werden sollen. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jedes Teil nach der Regel „outputFile_partIndex.extension“ zu generieren.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne TIFF-Datei mit mehreren Frames gespeichert.

## Beispiele

Zeigt, wie Sie aus einem DataSet einen Serienbrief mit Regionen-Operation durchführen.

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

MailMerger.ExecuteWithRegions(doc, ArtifactsDir + "LowCode.MailMergeWithRegionsDataSet.1.docx", dataSet);
MailMerger.ExecuteWithRegions(doc, ArtifactsDir + "LowCode.MailMergeWithRegionsDataSet.2.docx", SaveFormat.Docx, dataSet);
MailMerger.ExecuteWithRegions(doc, ArtifactsDir + "LowCode.MailMergeWithRegionsDataSet.3.docx", SaveFormat.Docx, dataSet, new MailMergeOptions() { TrimWhitespaces = true });
```

### Siehe auch

* class [MailMerger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## ExecuteWithRegions(*string, string, [SaveFormat](../../../aspose.words/saveformat/), DataSet, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregions_4}

Führt einen Seriendruck aus einem DataSet in das Dokument mit Seriendruckbereichen aus.

```csharp
public static void ExecuteWithRegions(string inputFileName, string outputFileName, 
    SaveFormat saveFormat, DataSet dataSet, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| outputFileName | String | Der Name der Ausgabedatei. |
| saveFormat | SaveFormat | Das Speicherformat der Ausgabe. |
| dataSet | DataSet | DataSet, das Daten enthält, die in Serienbrieffelder eingefügt werden sollen. |
| mailMergeOptions | MailMergeOptions | Optionen für Serienbriefe. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jedes Teil nach der Regel „outputFile_partIndex.extension“ zu generieren.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne TIFF-Datei mit mehreren Frames gespeichert.

## Beispiele

Zeigt, wie Sie aus einem DataSet einen Serienbrief mit Regionen-Operation durchführen.

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

MailMerger.ExecuteWithRegions(doc, ArtifactsDir + "LowCode.MailMergeWithRegionsDataSet.1.docx", dataSet);
MailMerger.ExecuteWithRegions(doc, ArtifactsDir + "LowCode.MailMergeWithRegionsDataSet.2.docx", SaveFormat.Docx, dataSet);
MailMerger.ExecuteWithRegions(doc, ArtifactsDir + "LowCode.MailMergeWithRegionsDataSet.3.docx", SaveFormat.Docx, dataSet, new MailMergeOptions() { TrimWhitespaces = true });
```

### Siehe auch

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## ExecuteWithRegions(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), DataSet, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregions_6}

Führt einen Seriendruck aus einem DataSet in das Dokument mit Seriendruckbereichen aus.

```csharp
public static void ExecuteWithRegions(string inputFileName, string outputFileName, 
    SaveOptions saveOptions, DataSet dataSet, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| outputFileName | String | Der Name der Ausgabedatei. |
| saveOptions | SaveOptions | Die Speicheroptionen der Ausgabe. |
| dataSet | DataSet | DataSet, das Daten enthält, die in Serienbrieffelder eingefügt werden sollen. |
| mailMergeOptions | MailMergeOptions | Optionen für Serienbriefe. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jedes Teil nach der Regel „outputFile_partIndex.extension“ zu generieren.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne TIFF-Datei mit mehreren Frames gespeichert.

### Siehe auch

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## ExecuteWithRegions(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), DataSet, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregions}

Führt einen Seriendruck aus einem DataSet in das Dokument mit Seriendruckbereichen aus.

```csharp
public static void ExecuteWithRegions(Stream inputStream, Stream outputStream, 
    SaveFormat saveFormat, DataSet dataSet, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | Stream | Der Eingabedateistream. |
| outputStream | Stream | Der Ausgabedateistream. |
| saveFormat | SaveFormat | Das Speicherformat der Ausgabe. |
| dataSet | DataSet | DataSet, das Daten enthält, die in Serienbrieffelder eingefügt werden sollen. |
| mailMergeOptions | MailMergeOptions | Optionen für Serienbriefe. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe im angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelnes TIFF mit mehreren Frames im angegebenen Stream gespeichert.

## Beispiele

Zeigt, wie Sie mithilfe von Dokumenten aus dem Stream einen Serienbrief mit Regionen-Operation aus einem DataSet heraus durchführen.

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
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeStreamWithRegionsDataTable.1.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.ExecuteWithRegions(streamIn, streamOut, SaveFormat.Docx, dataSet);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeStreamWithRegionsDataTable.2.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.ExecuteWithRegions(streamIn, streamOut, SaveFormat.Docx, dataSet, new MailMergeOptions() { TrimWhitespaces = true });
}
```

### Siehe auch

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## ExecuteWithRegions(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), DataSet, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregions_2}

Führt einen Seriendruck aus einem DataSet in das Dokument mit Seriendruckbereichen aus.

```csharp
public static void ExecuteWithRegions(Stream inputStream, Stream outputStream, 
    SaveOptions saveOptions, DataSet dataSet, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | Stream | Der Eingabedateistream. |
| outputStream | Stream | Der Ausgabedateistream. |
| saveOptions | SaveOptions | Die Speicheroptionen der Ausgabe. |
| dataSet | DataSet | DataSet, das Daten enthält, die in Serienbrieffelder eingefügt werden sollen. |
| mailMergeOptions | MailMergeOptions | Optionen für Serienbriefe. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe im angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelnes TIFF mit mehreren Frames im angegebenen Stream gespeichert.

### Siehe auch

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)
