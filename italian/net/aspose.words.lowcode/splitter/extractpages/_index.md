---
title: Splitter.ExtractPages
linktitle: ExtractPages
articleTitle: ExtractPages
second_title: Aspose.Words per .NET
description: Estrai facilmente pagine specifiche da qualsiasi documento con il nostro metodo Splitter ExtractPages. Salvale nel formato desiderato per un facile accesso!
type: docs
weight: 20
url: /it/net/aspose.words.lowcode/splitter/extractpages/
---
## ExtractPages(*string, string, int, int*) {#extractpages_4}

Estrae un intervallo specificato di pagine da un file di documento e salva le pagine estratte in un nuovo file. Il formato del file di output è determinato dall'estensione del nome del file di output.

```csharp
public static void ExtractPages(string inputFileName, string outputFileName, int startPageIndex, 
    int pageCount)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | String | Nome del file di input. |
| outputFileName | String | Nome del file di output. |
| startPageIndex | Int32 | Indice a partire da zero della prima pagina da estrarre. |
| pageCount | Int32 | Numero di pagine da estrarre. |

## Esempi

Mostra come estrarre le pagine dal documento.

```csharp
// Esistono diversi modi per estrarre le pagine dal documento:
string doc = MyDir + "Big document.docx";

Splitter.ExtractPages(doc, ArtifactsDir + "LowCode.ExtractPages.1.docx", 0, 2);
Splitter.ExtractPages(doc, ArtifactsDir + "LowCode.ExtractPages.2.docx", SaveFormat.Docx, 0, 2);
```

### Guarda anche

* class [Splitter](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## ExtractPages(*string, string, [SaveFormat](../../../aspose.words/saveformat/), int, int*) {#extractpages_2}

Estrae un intervallo specificato di pagine da un file di documento e salva le pagine estratte in un nuovo file utilizzando il formato di salvataggio specificato.

```csharp
public static void ExtractPages(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    int startPageIndex, int pageCount)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | String | Nome del file di input. |
| outputFileName | String | Nome del file di output. |
| saveFormat | SaveFormat | Formato di salvataggio. |
| startPageIndex | Int32 | Indice a partire da zero della prima pagina da estrarre. |
| pageCount | Int32 | Numero di pagine da estrarre. |

## Esempi

Mostra come estrarre le pagine dal documento.

```csharp
// Esistono diversi modi per estrarre le pagine dal documento:
string doc = MyDir + "Big document.docx";

Splitter.ExtractPages(doc, ArtifactsDir + "LowCode.ExtractPages.1.docx", 0, 2);
Splitter.ExtractPages(doc, ArtifactsDir + "LowCode.ExtractPages.2.docx", SaveFormat.Docx, 0, 2);
```

### Guarda anche

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Splitter](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## ExtractPages(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), int, int*) {#extractpages_3}

Estrae un intervallo specificato di pagine da un file di documento e salva le pagine estratte in un nuovo file utilizzando il formato di salvataggio specificato.

```csharp
public static void ExtractPages(string inputFileName, string outputFileName, 
    SaveOptions saveOptions, int startPageIndex, int pageCount)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | String | Nome del file di input. |
| outputFileName | String | Nome del file di output. |
| saveOptions | SaveOptions | Le opzioni di salvataggio. |
| startPageIndex | Int32 | Indice a partire da zero della prima pagina da estrarre. |
| pageCount | Int32 | Numero di pagine da estrarre. |

### Guarda anche

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Splitter](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## ExtractPages(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), int, int*) {#extractpages}

Estrae un intervallo specificato di pagine da un flusso di documenti e salva le pagine estratte in un flusso di output utilizzando il formato di salvataggio specificato.

```csharp
public static void ExtractPages(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    int startPageIndex, int pageCount)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | Stream | Il flusso di input. |
| outputStream | Stream | Il flusso di output. |
| saveFormat | SaveFormat | Formato di salvataggio. |
| startPageIndex | Int32 | Indice a partire da zero della prima pagina da estrarre. |
| pageCount | Int32 | Numero di pagine da estrarre. |

## Esempi

Mostra come estrarre le pagine del documento dal flusso.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ExtractPagesStream.docx", FileMode.Create, FileAccess.ReadWrite))
        Splitter.ExtractPages(streamIn, streamOut, SaveFormat.Docx, 0, 2);
}
```

### Guarda anche

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Splitter](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## ExtractPages(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), int, int*) {#extractpages_1}

Estrae un intervallo specificato di pagine da un flusso di documenti e salva le pagine estratte in un flusso di output utilizzando il formato di salvataggio specificato.

```csharp
public static void ExtractPages(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    int startPageIndex, int pageCount)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | Stream | Il flusso di input. |
| outputStream | Stream | Il flusso di output. |
| saveOptions | SaveOptions | Le opzioni di salvataggio. |
| startPageIndex | Int32 | Indice a partire da zero della prima pagina da estrarre. |
| pageCount | Int32 | Numero di pagine da estrarre. |

### Guarda anche

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Splitter](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)
