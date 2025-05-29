---
title: MailMerger.Execute
linktitle: Execute
articleTitle: Execute
second_title: Aspose.Words per .NET
description: Semplifica il tuo flusso di lavoro con il metodo MailMerger Execute, unendo senza sforzo i dati dei singoli record per migliorare l'efficienza e la precisione.
type: docs
weight: 20
url: /it/net/aspose.words.lowcode/mailmerger/execute/
---
## Execute(*string, string, string[], object[]*) {#execute_14}

Esegue un'operazione di unione di posta per un singolo record.

```csharp
public static void Execute(string inputFileName, string outputFileName, string[] fieldNames, 
    object[] fieldValues)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | String | Nome del file di input. |
| outputFileName | String | Nome del file di output. |
| fieldNames | String[] | Array di nomi di campi unione. I nomi dei campi non fanno distinzione tra maiuscole e minuscole. Se viene rilevato un nome di campo non presente nel documento, viene ignorato. |
| fieldValues | Object[] | Array di valori da inserire nei campi di unione. Il numero di elementi in questo array deve essere uguale al numero di elementi in fieldNames. |

## Osservazioni

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà utilizzato per generare i nomi file per ogni parte, seguendo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un singolo file TIFF multi-frame.

## Esempi

Mostra come eseguire un'operazione di stampa unione per un singolo record.

```csharp
// Esistono diversi modi per eseguire un'operazione di unione di posta:
string doc = MyDir + "Mail merge.doc";

string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.1.docx", fieldNames, fieldValues);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.2.docx", SaveFormat.Docx, fieldNames, fieldValues);
MailMergeOptions mailMergeOptions = new MailMergeOptions();
mailMergeOptions.TrimWhitespaces = true;
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.3.docx", SaveFormat.Docx, fieldNames, fieldValues, mailMergeOptions);
```

### Guarda anche

* class [MailMerger](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## Execute(*string, string, [SaveFormat](../../../aspose.words/saveformat/), string[], object[], [MailMergeOptions](../../mailmergeoptions/)*) {#execute_8}

Esegue un'operazione di unione di posta per un singolo record.

```csharp
public static void Execute(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    string[] fieldNames, object[] fieldValues, MailMergeOptions mailMergeOptions = null)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | String | Nome del file di input. |
| outputFileName | String | Nome del file di output. |
| saveFormat | SaveFormat | Formato di salvataggio dell'output. |
| fieldNames | String[] | Array di nomi di campi unione. I nomi dei campi non fanno distinzione tra maiuscole e minuscole. Se viene rilevato un nome di campo non presente nel documento, viene ignorato. |
| fieldValues | Object[] | Array di valori da inserire nei campi di unione. Il numero di elementi in questo array deve essere uguale al numero di elementi in fieldNames. |
| mailMergeOptions | MailMergeOptions | Opzioni di unione posta. |

## Osservazioni

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà utilizzato per generare i nomi file per ogni parte, seguendo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un singolo file TIFF multi-frame.

## Esempi

Mostra come eseguire un'operazione di stampa unione per un singolo record.

```csharp
// Esistono diversi modi per eseguire un'operazione di unione di posta:
string doc = MyDir + "Mail merge.doc";

string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.1.docx", fieldNames, fieldValues);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.2.docx", SaveFormat.Docx, fieldNames, fieldValues);
MailMergeOptions mailMergeOptions = new MailMergeOptions();
mailMergeOptions.TrimWhitespaces = true;
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.3.docx", SaveFormat.Docx, fieldNames, fieldValues, mailMergeOptions);
```

### Guarda anche

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## Execute(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), string[], object[], [MailMergeOptions](../../mailmergeoptions/)*) {#execute_11}

Esegue un'operazione di unione di posta per un singolo record.

```csharp
public static void Execute(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    string[] fieldNames, object[] fieldValues, MailMergeOptions mailMergeOptions = null)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | String | Nome del file di input. |
| outputFileName | String | Nome del file di output. |
| saveOptions | SaveOptions | Opzioni di salvataggio dell'output. |
| fieldNames | String[] | Array di nomi di campi unione. I nomi dei campi non fanno distinzione tra maiuscole e minuscole. Se viene rilevato un nome di campo non presente nel documento, viene ignorato. |
| fieldValues | Object[] | Array di valori da inserire nei campi di unione. Il numero di elementi in questo array deve essere uguale al numero di elementi in fieldNames. |
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

## Execute(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), string[], object[], [MailMergeOptions](../../mailmergeoptions/)*) {#execute_2}

Esegue un'operazione di unione di posta per un singolo record.

```csharp
public static void Execute(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    string[] fieldNames, object[] fieldValues, MailMergeOptions mailMergeOptions = null)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | Stream | Flusso del file di input. |
| outputStream | Stream | Flusso del file di output. |
| saveFormat | SaveFormat | Formato di salvataggio dell'output. |
| fieldNames | String[] | Array di nomi di campi unione. I nomi dei campi non fanno distinzione tra maiuscole e minuscole. Se viene rilevato un nome di campo non presente nel documento, viene ignorato. |
| fieldValues | Object[] | Array di valori da inserire nei campi di unione. Il numero di elementi in questo array deve essere uguale al numero di elementi in fieldNames. |
| mailMergeOptions | MailMergeOptions | Opzioni di unione posta. |

## Osservazioni

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la prima pagina dell'output verrà salvata nel flusso specificato.

Se il formato di output è TIFF, l'output verrà salvato come un singolo TIFF multi-frame nel flusso specificato.

## Esempi

Mostra come eseguire un'operazione di stampa unione per un singolo record dal flusso.

```csharp
// Esistono diversi modi per eseguire un'operazione di unione di posta utilizzando i documenti dal flusso:
string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.Execute(streamIn, streamOut, SaveFormat.Docx, fieldNames, fieldValues);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
    {
        MailMergeOptions mailMergeOptions = new MailMergeOptions();
        mailMergeOptions.TrimWhitespaces = true;
        MailMerger.Execute(streamIn, streamOut, SaveFormat.Docx, fieldNames, fieldValues, mailMergeOptions);
    }
}
```

### Guarda anche

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## Execute(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), string[], object[], [MailMergeOptions](../../mailmergeoptions/)*) {#execute_5}

Esegue un'operazione di unione di posta per un singolo record.

```csharp
public static void Execute(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    string[] fieldNames, object[] fieldValues, MailMergeOptions mailMergeOptions = null)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | Stream | Flusso del file di input. |
| outputStream | Stream | Flusso del file di output. |
| saveOptions | SaveOptions | Opzioni di salvataggio dell'output. |
| fieldNames | String[] | Array di nomi di campi unione. I nomi dei campi non fanno distinzione tra maiuscole e minuscole. Se viene rilevato un nome di campo non presente nel documento, viene ignorato. |
| fieldValues | Object[] | Array di valori da inserire nei campi di unione. Il numero di elementi in questo array deve essere uguale al numero di elementi in fieldNames. |
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

## Execute(*string, string, DataRow*) {#execute_12}

Esegue la stampa unione da un DataRow nel documento.

```csharp
public static void Execute(string inputFileName, string outputFileName, DataRow dataRow)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | String | Nome del file di input. |
| outputFileName | String | Nome del file di output. |
| dataRow | DataRow | Riga contenente i dati da inserire nei campi di stampa unione. I nomi dei campi non fanno distinzione tra maiuscole e minuscole. Se viene rilevato un nome di campo non presente nel documento, viene ignorato. |

## Osservazioni

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà utilizzato per generare i nomi file per ogni parte, seguendo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un singolo file TIFF multi-frame.

## Esempi

Mostra come eseguire un'operazione di stampa unione da un DataRow.

```csharp
// Esistono diversi modi per eseguire un'operazione di stampa unione da un DataRow:
string doc = MyDir + "Mail merge.doc";

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMergeDataRow.1.docx", dataRow);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMergeDataRow.2.docx", SaveFormat.Docx, dataRow);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMergeDataRow.3.docx", SaveFormat.Docx, dataRow, new MailMergeOptions() { TrimWhitespaces = true });
```

### Guarda anche

* class [MailMerger](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## Execute(*string, string, [SaveFormat](../../../aspose.words/saveformat/), DataRow, [MailMergeOptions](../../mailmergeoptions/)*) {#execute_6}

Esegue la stampa unione da un DataRow nel documento.

```csharp
public static void Execute(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    DataRow dataRow, MailMergeOptions mailMergeOptions = null)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | String | Nome del file di input. |
| outputFileName | String | Nome del file di output. |
| saveFormat | SaveFormat | Formato di salvataggio dell'output. |
| dataRow | DataRow | Riga contenente i dati da inserire nei campi di stampa unione. I nomi dei campi non fanno distinzione tra maiuscole e minuscole. Se viene rilevato un nome di campo non presente nel documento, viene ignorato. |
| mailMergeOptions | MailMergeOptions | Opzioni di unione posta. |

## Osservazioni

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà utilizzato per generare i nomi file per ogni parte, seguendo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un singolo file TIFF multi-frame.

## Esempi

Mostra come eseguire un'operazione di stampa unione da un DataRow.

```csharp
// Esistono diversi modi per eseguire un'operazione di stampa unione da un DataRow:
string doc = MyDir + "Mail merge.doc";

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMergeDataRow.1.docx", dataRow);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMergeDataRow.2.docx", SaveFormat.Docx, dataRow);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMergeDataRow.3.docx", SaveFormat.Docx, dataRow, new MailMergeOptions() { TrimWhitespaces = true });
```

### Guarda anche

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## Execute(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), DataRow, [MailMergeOptions](../../mailmergeoptions/)*) {#execute_9}

Esegue la stampa unione da un DataRow nel documento.

```csharp
public static void Execute(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    DataRow dataRow, MailMergeOptions mailMergeOptions = null)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | String | Nome del file di input. |
| outputFileName | String | Nome del file di output. |
| saveOptions | SaveOptions | Opzioni di salvataggio dell'output. |
| dataRow | DataRow | Riga contenente i dati da inserire nei campi di stampa unione. I nomi dei campi non fanno distinzione tra maiuscole e minuscole. Se viene rilevato un nome di campo non presente nel documento, viene ignorato. |
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

## Execute(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), DataRow, [MailMergeOptions](../../mailmergeoptions/)*) {#execute}

Esegue un'operazione di unione di posta per un singolo record.

```csharp
public static void Execute(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    DataRow dataRow, MailMergeOptions mailMergeOptions = null)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | Stream | Flusso del file di input. |
| outputStream | Stream | Flusso del file di output. |
| saveFormat | SaveFormat | Formato di salvataggio dell'output. |
| dataRow | DataRow | Riga contenente i dati da inserire nei campi di stampa unione. I nomi dei campi non fanno distinzione tra maiuscole e minuscole. Se viene rilevato un nome di campo non presente nel documento, viene ignorato. |
| mailMergeOptions | MailMergeOptions | Opzioni di unione posta. |

## Osservazioni

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la prima pagina dell'output verrà salvata nel flusso specificato.

Se il formato di output è TIFF, l'output verrà salvato come un singolo TIFF multi-frame nel flusso specificato.

## Esempi

Mostra come eseguire un'operazione di stampa unione da un DataRow utilizzando i documenti dal flusso.

```csharp
// Esistono diversi modi per eseguire un'operazione di unione di posta da un DataRow utilizzando i documenti dal flusso:
DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeStreamDataRow.1.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.Execute(streamIn, streamOut, SaveFormat.Docx, dataRow);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeStreamDataRow.2.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.Execute(streamIn, streamOut, SaveFormat.Docx, dataRow, new MailMergeOptions() { TrimWhitespaces = true });
}
```

### Guarda anche

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## Execute(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), DataRow, [MailMergeOptions](../../mailmergeoptions/)*) {#execute_3}

Esegue un'operazione di unione di posta per un singolo record.

```csharp
public static void Execute(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    DataRow dataRow, MailMergeOptions mailMergeOptions = null)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | Stream | Flusso del file di input. |
| outputStream | Stream | Flusso del file di output. |
| saveOptions | SaveOptions | Opzioni di salvataggio dell'output. |
| dataRow | DataRow | Riga contenente i dati da inserire nei campi di stampa unione. I nomi dei campi non fanno distinzione tra maiuscole e minuscole. Se viene rilevato un nome di campo non presente nel documento, viene ignorato. |
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

## Execute(*string, string, DataTable*) {#execute_13}

Esegue la stampa unione da una tabella dati nel documento.

```csharp
public static void Execute(string inputFileName, string outputFileName, DataTable dataTable)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | String | Nome del file di input. |
| outputFileName | String | Nome del file di output. |
| dataTable | DataTable | Tabella contenente i dati da inserire nei campi di stampa unione. I nomi dei campi non fanno distinzione tra maiuscole e minuscole. Se viene rilevato un nome di campo non presente nel documento, viene ignorato. |

## Osservazioni

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà utilizzato per generare i nomi file per ogni parte, seguendo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un singolo file TIFF multi-frame.

## Esempi

Mostra come eseguire un'operazione di stampa unione da una tabella dati.

```csharp
// Esistono diversi modi per eseguire un'operazione di stampa unione da una tabella dati:
string doc = MyDir + "Mail merge.doc";

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMergeDataTable.1.docx", dataTable);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMergeDataTable.2.docx", SaveFormat.Docx, dataTable);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMergeDataTable.3.docx", SaveFormat.Docx, dataTable, new MailMergeOptions() { TrimWhitespaces = true });
```

### Guarda anche

* class [MailMerger](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## Execute(*string, string, [SaveFormat](../../../aspose.words/saveformat/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#execute_7}

Esegue la stampa unione da un DataRow nel documento.

```csharp
public static void Execute(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    DataTable dataTable, MailMergeOptions mailMergeOptions = null)
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

Mostra come eseguire un'operazione di stampa unione da una tabella dati.

```csharp
// Esistono diversi modi per eseguire un'operazione di stampa unione da una tabella dati:
string doc = MyDir + "Mail merge.doc";

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMergeDataTable.1.docx", dataTable);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMergeDataTable.2.docx", SaveFormat.Docx, dataTable);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMergeDataTable.3.docx", SaveFormat.Docx, dataTable, new MailMergeOptions() { TrimWhitespaces = true });
```

### Guarda anche

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## Execute(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#execute_10}

Esegue la stampa unione da un DataRow nel documento.

```csharp
public static void Execute(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    DataTable dataTable, MailMergeOptions mailMergeOptions = null)
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

## Execute(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#execute_1}

Esegue un'operazione di unione di posta per un singolo record.

```csharp
public static void Execute(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    DataTable dataTable, MailMergeOptions mailMergeOptions = null)
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

Mostra come eseguire un'operazione di stampa unione da una tabella dati utilizzando i documenti del flusso.

```csharp
// Esistono diversi modi per eseguire un'operazione di unione di posta da una DataTable utilizzando i documenti dal flusso:
DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeDataTable.1.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.Execute(streamIn, streamOut, SaveFormat.Docx, dataTable);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeDataTable.2.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.Execute(streamIn, streamOut, SaveFormat.Docx, dataTable, new MailMergeOptions() { TrimWhitespaces = true });
}
```

### Guarda anche

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## Execute(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#execute_4}

Esegue un'operazione di unione di posta per un singolo record.

```csharp
public static void Execute(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    DataTable dataTable, MailMergeOptions mailMergeOptions = null)
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
