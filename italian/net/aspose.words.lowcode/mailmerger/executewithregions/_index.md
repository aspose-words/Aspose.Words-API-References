---
title: MailMerger.ExecuteWithRegions
linktitle: ExecuteWithRegions
articleTitle: ExecuteWithRegions
second_title: Aspose.Words per .NET
description: Semplifica la creazione dei tuoi documenti con il metodo ExecuteWithRegions di MailMerger. Unisci facilmente le DataTable nei documenti utilizzando regioni personalizzabili.
type: docs
weight: 40
url: /it/net/aspose.words.lowcode/mailmerger/executewithregions/
---
## ExecuteWithRegions(*string, string, DataTable*) {#executewithregions_9}

Esegue la stampa unione da una tabella dati nel documento con aree di stampa unione.

```csharp
public static void ExecuteWithRegions(string inputFileName, string outputFileName, 
    DataTable dataTable)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | String | Nome del file di input. |
| outputFileName | String | Nome del file di output. |
| dataTable | DataTable | Origine dati per l'operazione di stampa unione. La tabella deve avere la proprietà TableName impostata. |

## Osservazioni

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà utilizzato per generare i nomi file per ogni parte, seguendo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un singolo file TIFF multi-frame.

## Esempi

Mostra come eseguire un'operazione di stampa unione con regioni da una tabella dati.

```csharp
// Esistono diversi modi per eseguire un'operazione di stampa unione con regioni da una DataTable:
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

### Guarda anche

* class [MailMerger](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## ExecuteWithRegions(*string, string, [SaveFormat](../../../aspose.words/saveformat/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregions_5}

Esegue la stampa unione da una tabella dati nel documento con aree di stampa unione.

```csharp
public static void ExecuteWithRegions(string inputFileName, string outputFileName, 
    SaveFormat saveFormat, DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | String | Nome del file di input. |
| outputFileName | String | Nome del file di output. |
| saveFormat | SaveFormat | Formato di salvataggio dell'output. |
| dataTable | DataTable | Tabella contenente i dati da inserire nei campi di stampa unione. I nomi dei campi non fanno distinzione tra maiuscole e minuscole. Se viene rilevato un nome di campo non presente nel documento, viene ignorato. |
| mailMergeOptions | MailMergeOptions | Opzioni di unione posta. |

## Osservazioni

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà utilizzato per generare i nomi file per ogni parte, seguendo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un singolo file TIFF multi-frame.

## Esempi

Mostra come eseguire un'operazione di stampa unione con regioni da una tabella dati.

```csharp
// Esistono diversi modi per eseguire un'operazione di stampa unione con regioni da una DataTable:
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

### Guarda anche

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## ExecuteWithRegions(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregions_7}

Esegue la stampa unione da una tabella dati nel documento con aree di stampa unione.

```csharp
public static void ExecuteWithRegions(string inputFileName, string outputFileName, 
    SaveOptions saveOptions, DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | String | Nome del file di input. |
| outputFileName | String | Nome del file di output. |
| saveOptions | SaveOptions | Opzioni di salvataggio dell'output. |
| dataTable | DataTable | Tabella contenente i dati da inserire nei campi di stampa unione. I nomi dei campi non fanno distinzione tra maiuscole e minuscole. Se viene rilevato un nome di campo non presente nel documento, viene ignorato. |
| mailMergeOptions | MailMergeOptions | Opzioni di unione posta. |

## Osservazioni

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà utilizzato per generare i nomi file per ogni parte, seguendo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un singolo file TIFF multi-frame.

### Guarda anche

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## ExecuteWithRegions(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregions_1}

Esegue un'operazione di unione di posta per un singolo record.

```csharp
public static void ExecuteWithRegions(Stream inputStream, Stream outputStream, 
    SaveFormat saveFormat, DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | Stream | Flusso del file di input. |
| outputStream | Stream | Flusso del file di output. |
| saveFormat | SaveFormat | Formato di salvataggio dell'output. |
| dataTable | DataTable | Tabella contenente i dati da inserire nei campi di stampa unione. I nomi dei campi non fanno distinzione tra maiuscole e minuscole. Se viene rilevato un nome di campo non presente nel documento, viene ignorato. |
| mailMergeOptions | MailMergeOptions | Opzioni di unione posta. |

## Osservazioni

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la prima pagina dell'output verrà salvata nel flusso specificato.

Se il formato di output è TIFF, l'output verrà salvato come un singolo TIFF multi-frame nel flusso specificato.

## Esempi

Mostra come eseguire un'operazione di unione di stampe con regioni da una tabella dati utilizzando i documenti del flusso.

```csharp
// Esistono diversi modi per eseguire un'operazione di unione di posta con regioni da una DataTable utilizzando i documenti dal flusso:
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

### Guarda anche

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## ExecuteWithRegions(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregions_3}

Esegue un'operazione di unione di posta per un singolo record.

```csharp
public static void ExecuteWithRegions(Stream inputStream, Stream outputStream, 
    SaveOptions saveOptions, DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | Stream | Flusso del file di input. |
| outputStream | Stream | Flusso del file di output. |
| saveOptions | SaveOptions | Opzioni di salvataggio dell'output. |
| dataTable | DataTable | Tabella contenente i dati da inserire nei campi di stampa unione. I nomi dei campi non fanno distinzione tra maiuscole e minuscole. Se viene rilevato un nome di campo non presente nel documento, viene ignorato. |
| mailMergeOptions | MailMergeOptions | Opzioni di unione posta. |

## Osservazioni

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la prima pagina dell'output verrà salvata nel flusso specificato.

Se il formato di output è TIFF, l'output verrà salvato come un singolo TIFF multi-frame nel flusso specificato.

### Guarda anche

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## ExecuteWithRegions(*string, string, DataSet*) {#executewithregions_8}

Esegue la stampa unione da un DataSet in un documento con aree di stampa unione.

```csharp
public static void ExecuteWithRegions(string inputFileName, string outputFileName, DataSet dataSet)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | String | Nome del file di input. |
| outputFileName | String | Nome del file di output. |
| dataSet | DataSet | DataSet contenente i dati da inserire nei campi di stampa unione. |

## Osservazioni

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà utilizzato per generare i nomi file per ogni parte, seguendo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un singolo file TIFF multi-frame.

## Esempi

Mostra come eseguire un'operazione di stampa unione con regioni da un DataSet.

```csharp
// Esistono diversi modi per eseguire un'operazione di unione di posta con regioni da un DataSet:
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

### Guarda anche

* class [MailMerger](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## ExecuteWithRegions(*string, string, [SaveFormat](../../../aspose.words/saveformat/), DataSet, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregions_4}

Esegue la stampa unione da un DataSet nel documento con aree di stampa unione.

```csharp
public static void ExecuteWithRegions(string inputFileName, string outputFileName, 
    SaveFormat saveFormat, DataSet dataSet, MailMergeOptions mailMergeOptions = null)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | String | Nome del file di input. |
| outputFileName | String | Nome del file di output. |
| saveFormat | SaveFormat | Formato di salvataggio dell'output. |
| dataSet | DataSet | DataSet contenente i dati da inserire nei campi di stampa unione. |
| mailMergeOptions | MailMergeOptions | Opzioni di unione posta. |

## Osservazioni

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà utilizzato per generare i nomi file per ogni parte, seguendo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un singolo file TIFF multi-frame.

## Esempi

Mostra come eseguire un'operazione di stampa unione con regioni da un DataSet.

```csharp
// Esistono diversi modi per eseguire un'operazione di unione di posta con regioni da un DataSet:
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

### Guarda anche

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## ExecuteWithRegions(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), DataSet, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregions_6}

Esegue la stampa unione da un DataSet nel documento con aree di stampa unione.

```csharp
public static void ExecuteWithRegions(string inputFileName, string outputFileName, 
    SaveOptions saveOptions, DataSet dataSet, MailMergeOptions mailMergeOptions = null)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | String | Nome del file di input. |
| outputFileName | String | Nome del file di output. |
| saveOptions | SaveOptions | Opzioni di salvataggio dell'output. |
| dataSet | DataSet | DataSet contenente i dati da inserire nei campi di stampa unione. |
| mailMergeOptions | MailMergeOptions | Opzioni di unione posta. |

## Osservazioni

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà utilizzato per generare i nomi file per ogni parte, seguendo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un singolo file TIFF multi-frame.

### Guarda anche

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## ExecuteWithRegions(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), DataSet, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregions}

Esegue la stampa unione da un DataSet nel documento con aree di stampa unione.

```csharp
public static void ExecuteWithRegions(Stream inputStream, Stream outputStream, 
    SaveFormat saveFormat, DataSet dataSet, MailMergeOptions mailMergeOptions = null)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | Stream | Flusso del file di input. |
| outputStream | Stream | Flusso del file di output. |
| saveFormat | SaveFormat | Formato di salvataggio dell'output. |
| dataSet | DataSet | DataSet contenente i dati da inserire nei campi di stampa unione. |
| mailMergeOptions | MailMergeOptions | Opzioni di unione posta. |

## Osservazioni

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la prima pagina dell'output verrà salvata nel flusso specificato.

Se il formato di output è TIFF, l'output verrà salvato come un singolo TIFF multi-frame nel flusso specificato.

## Esempi

Mostra come eseguire un'operazione di unione di stampe con regioni da un DataSet utilizzando i documenti del flusso.

```csharp
// Esistono diversi modi per eseguire un'operazione di unione di posta con regioni da un DataSet utilizzando i documenti dal flusso:
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

### Guarda anche

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## ExecuteWithRegions(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), DataSet, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregions_2}

Esegue la stampa unione da un DataSet nel documento con aree di stampa unione.

```csharp
public static void ExecuteWithRegions(Stream inputStream, Stream outputStream, 
    SaveOptions saveOptions, DataSet dataSet, MailMergeOptions mailMergeOptions = null)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | Stream | Flusso del file di input. |
| outputStream | Stream | Flusso del file di output. |
| saveOptions | SaveOptions | Opzioni di salvataggio dell'output. |
| dataSet | DataSet | DataSet contenente i dati da inserire nei campi di stampa unione. |
| mailMergeOptions | MailMergeOptions | Opzioni di unione posta. |

## Osservazioni

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la prima pagina dell'output verrà salvata nel flusso specificato.

Se il formato di output è TIFF, l'output verrà salvato come un singolo TIFF multi-frame nel flusso specificato.

### Guarda anche

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)
