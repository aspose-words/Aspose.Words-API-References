---
title: MailMerger.ExecuteToImages
linktitle: ExecuteToImages
articleTitle: ExecuteToImages
second_title: Aspose.Words per .NET
description: Esegui senza sforzo una stampa unione di record individuali e converti i risultati in immagini di alta qualità con il metodo MailMerger ExecuteToImages.
type: docs
weight: 30
url: /it/net/aspose.words.lowcode/mailmerger/executetoimages/
---
## ExecuteToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string[], object[], [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages_5}

Esegue un'operazione di unione di posta per un singolo record e restituisce il risultato in immagini.

```csharp
public static Stream[] ExecuteToImages(string inputFileName, ImageSaveOptions saveOptions, 
    string[] fieldNames, object[] fieldValues, MailMergeOptions mailMergeOptions = null)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | String | Nome del file di input. |
| saveOptions | ImageSaveOptions | Opzioni di salvataggio dell'output. |
| fieldNames | String[] | Array di nomi di campi unione. I nomi dei campi non fanno distinzione tra maiuscole e minuscole. Se viene rilevato un nome di campo non presente nel documento, viene ignorato. |
| fieldValues | Object[] | Array di valori da inserire nei campi di unione. Il numero di elementi in questo array deve essere uguale al numero di elementi in fieldNames. |
| mailMergeOptions | MailMergeOptions | Opzioni di unione posta. |

## Esempi

Mostra come eseguire un'operazione di stampa unione per un singolo record e salvare il risultato come immagini.

```csharp
// Esistono diversi modi per eseguire un'operazione di unione di posta:
string doc = MyDir + "Mail merge.doc";

string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

Stream[] images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), fieldNames, fieldValues);
MailMergeOptions mailMergeOptions = new MailMergeOptions();
mailMergeOptions.TrimWhitespaces = true;
images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), fieldNames, fieldValues, mailMergeOptions);
```

### Guarda anche

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## ExecuteToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string[], object[], [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages_2}

Esegue un'operazione di unione di posta per un singolo record e restituisce il risultato in immagini.

```csharp
public static Stream[] ExecuteToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    string[] fieldNames, object[] fieldValues, MailMergeOptions mailMergeOptions = null)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | Stream | Flusso del file di input. |
| saveOptions | ImageSaveOptions | Opzioni di salvataggio dell'output. |
| fieldNames | String[] | Array di nomi di campi unione. I nomi dei campi non fanno distinzione tra maiuscole e minuscole. Se viene rilevato un nome di campo non presente nel documento, viene ignorato. |
| fieldValues | Object[] | Array di valori da inserire nei campi di unione. Il numero di elementi in questo array deve essere uguale al numero di elementi in fieldNames. |
| mailMergeOptions | MailMergeOptions | Opzioni di unione posta. |

## Esempi

Mostra come eseguire un'operazione di unione di dati per un singolo record dal flusso e salvare il risultato come immagini.

```csharp
// Esistono diversi modi per eseguire un'operazione di unione di posta utilizzando i documenti dal flusso:
string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    Stream[] images = MailMerger.ExecuteToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), fieldNames, fieldValues);

    MailMergeOptions mailMergeOptions = new MailMergeOptions();
    mailMergeOptions.TrimWhitespaces = true;
    images = MailMerger.ExecuteToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), fieldNames, fieldValues, mailMergeOptions);
}
```

### Guarda anche

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## ExecuteToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataRow, [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages_3}

Esegue la stampa unione da un DataRow nel documento e restituisce il risultato in immagini.

```csharp
public static Stream[] ExecuteToImages(string inputFileName, ImageSaveOptions saveOptions, 
    DataRow dataRow, MailMergeOptions mailMergeOptions = null)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | String | Nome del file di input. |
| saveOptions | ImageSaveOptions | Opzioni di salvataggio dell'output. |
| dataRow | DataRow | Riga contenente i dati da inserire nei campi di stampa unione. I nomi dei campi non fanno distinzione tra maiuscole e minuscole. Se viene rilevato un nome di campo non presente nel documento, viene ignorato. |
| mailMergeOptions | MailMergeOptions | Opzioni di unione posta. |

## Esempi

Mostra come eseguire un'operazione di stampa unione da un DataRow e salvare il risultato come immagini.

```csharp
// Esistono diversi modi per eseguire un'operazione di stampa unione da un DataRow:
string doc = MyDir + "Mail merge.doc";

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

Stream[] images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataRow);
images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataRow, new MailMergeOptions() { TrimWhitespaces = true });
```

### Guarda anche

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## ExecuteToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataRow, [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages}

Esegue la stampa unione da un DataRow nel documento e restituisce il risultato in immagini.

```csharp
public static Stream[] ExecuteToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    DataRow dataRow, MailMergeOptions mailMergeOptions = null)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | Stream | Flusso del file di input. |
| saveOptions | ImageSaveOptions | Opzioni di salvataggio dell'output. |
| dataRow | DataRow | Riga contenente i dati da inserire nei campi di stampa unione. I nomi dei campi non fanno distinzione tra maiuscole e minuscole. Se viene rilevato un nome di campo non presente nel documento, viene ignorato. |
| mailMergeOptions | MailMergeOptions | Opzioni di unione posta. |

## Esempi

Mostra come eseguire un'operazione di unione di dati da un DataRow utilizzando documenti dal flusso e salvare il risultato come immagini.

```csharp
// Esistono diversi modi per eseguire un'operazione di unione di posta da un DataRow utilizzando i documenti dal flusso:
DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    Stream[] images = MailMerger.ExecuteToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), dataRow);
    images = MailMerger.ExecuteToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), dataRow, new MailMergeOptions() { TrimWhitespaces = true });
}
```

### Guarda anche

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## ExecuteToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages_4}

Esegue la stampa unione da un DataRow nel documento e restituisce il risultato in immagini.

```csharp
public static Stream[] ExecuteToImages(string inputFileName, ImageSaveOptions saveOptions, 
    DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | String | Nome del file di input. |
| saveOptions | ImageSaveOptions | Opzioni di salvataggio dell'output. |
| dataTable | DataTable | Tabella contenente i dati da inserire nei campi di stampa unione. I nomi dei campi non fanno distinzione tra maiuscole e minuscole. Se viene rilevato un nome di campo non presente nel documento, viene ignorato. |
| mailMergeOptions | MailMergeOptions | Opzioni di unione posta. |

## Esempi

Mostra come eseguire un'operazione di stampa unione da una tabella dati e salvare il risultato in immagini.

```csharp
// Esistono diversi modi per eseguire un'operazione di stampa unione da una tabella dati:
string doc = MyDir + "Mail merge.doc";

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

Stream[] images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataTable);
images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataTable, new MailMergeOptions() { TrimWhitespaces = true });
```

### Guarda anche

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## ExecuteToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages_1}

Esegue la stampa unione da un DataRow nel documento e restituisce il risultato in immagini.

```csharp
public static Stream[] ExecuteToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | Stream | Flusso del file di input. |
| saveOptions | ImageSaveOptions | Opzioni di salvataggio dell'output. |
| dataTable | DataTable | Tabella contenente i dati da inserire nei campi di stampa unione. I nomi dei campi non fanno distinzione tra maiuscole e minuscole. Se viene rilevato un nome di campo non presente nel documento, viene ignorato. |
| mailMergeOptions | MailMergeOptions | Opzioni di unione posta. |

## Esempi

Mostra come eseguire un'operazione di unione di dati da una tabella dati utilizzando documenti dal flusso e salvandoli come immagini.

```csharp
// Esistono diversi modi per eseguire un'operazione di unione di posta da una DataTable utilizzando i documenti dal flusso e salvare il risultato in immagini:
DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    Stream[] images = MailMerger.ExecuteToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), dataTable);
    images = MailMerger.ExecuteToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), dataTable, new MailMergeOptions() { TrimWhitespaces = true });
}
```

### Guarda anche

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)
