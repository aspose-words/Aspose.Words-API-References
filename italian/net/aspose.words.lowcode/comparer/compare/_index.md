---
title: Comparer.Compare
linktitle: Compare
articleTitle: Compare
second_title: Aspose.Words per .NET
description: Confronta facilmente due documenti con il nostro metodo Compare. Salva le differenze e monitora le modifiche e le revisioni di formato in un unico file di output.
type: docs
weight: 20
url: /it/net/aspose.words.lowcode/comparer/compare/
---
## Compare(*string, string, string, string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#compare_4}

Confronta due documenti con opzioni aggiuntive e salva le differenze nel file di output specificato, producendo modifiche come un numero di revisioni di modifica e formato.

```csharp
public static void Compare(string v1, string v2, string outputFileName, string author, 
    DateTime dateTime, CompareOptions compareOptions = null)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| v1 | String | Il documento originale. |
| v2 | String | Il documento modificato. |
| outputFileName | String | Nome del file di output. |
| author | String | Iniziali dell'autore da utilizzare per le revisioni. |
| dateTime | DateTime | Data e ora da utilizzare per le revisioni. |
| compareOptions | CompareOptions | Opzioni di confronto dei documenti. |

## Osservazioni

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà utilizzato per generare i nomi file per ogni parte, seguendo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un singolo file TIFF multi-frame.

## Esempi

Mostra come confrontare in modo semplice i documenti.

```csharp
// Esistono diversi modi per confrontare i documenti:
string firstDoc = MyDir + "Table column bookmarks.docx";
string secondDoc = MyDir + "Table column bookmarks.doc";

Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.1.docx", "Author", new DateTime());
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.2.docx", SaveFormat.Docx, "Author", new DateTime());

CompareOptions compareOptions = new CompareOptions();
compareOptions.IgnoreCaseChanges = true;
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.3.docx", "Author", new DateTime(), compareOptions);
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.4.docx", SaveFormat.Docx, "Author", new DateTime(), compareOptions);
```

### Guarda anche

* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## Compare(*string, string, string, [SaveFormat](../../../aspose.words/saveformat/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#compare_2}

Confronta due documenti con opzioni aggiuntive e salva le differenze nel file di output specificato nel formato di salvataggio fornito, producendo modifiche come un numero di revisioni di modifica e formato.

```csharp
public static void Compare(string v1, string v2, string outputFileName, SaveFormat saveFormat, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| v1 | String | Il documento originale. |
| v2 | String | Il documento modificato. |
| outputFileName | String | Nome del file di output. |
| saveFormat | SaveFormat | Formato di salvataggio dell'output. |
| author | String | Iniziali dell'autore da utilizzare per le revisioni. |
| dateTime | DateTime | Data e ora da utilizzare per le revisioni. |
| compareOptions | CompareOptions | Opzioni di confronto dei documenti. |

## Osservazioni

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà utilizzato per generare i nomi file per ogni parte, seguendo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un singolo file TIFF multi-frame.

## Esempi

Mostra come confrontare in modo semplice i documenti.

```csharp
// Esistono diversi modi per confrontare i documenti:
string firstDoc = MyDir + "Table column bookmarks.docx";
string secondDoc = MyDir + "Table column bookmarks.doc";

Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.1.docx", "Author", new DateTime());
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.2.docx", SaveFormat.Docx, "Author", new DateTime());

CompareOptions compareOptions = new CompareOptions();
compareOptions.IgnoreCaseChanges = true;
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.3.docx", "Author", new DateTime(), compareOptions);
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.4.docx", SaveFormat.Docx, "Author", new DateTime(), compareOptions);
```

### Guarda anche

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## Compare(*string, string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#compare_3}

Confronta due documenti con opzioni aggiuntive e salva le differenze nel file di output specificato nel formato di salvataggio fornito, producendo modifiche come un numero di revisioni di modifica e formato.

```csharp
public static void Compare(string v1, string v2, string outputFileName, SaveOptions saveOptions, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| v1 | String | Il documento originale. |
| v2 | String | Il documento modificato. |
| outputFileName | String | Nome del file di output. |
| saveOptions | SaveOptions | Opzioni di salvataggio dell'output. |
| author | String | Iniziali dell'autore da utilizzare per le revisioni. |
| dateTime | DateTime | Data e ora da utilizzare per le revisioni. |
| compareOptions | CompareOptions | Opzioni di confronto dei documenti. |

## Osservazioni

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà utilizzato per generare i nomi file per ogni parte, seguendo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un singolo file TIFF multi-frame.

### Guarda anche

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## Compare(*Stream, Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#compare}

Confronta due documenti caricati da flussi con opzioni aggiuntive e salva le differenze nel flusso di output fornito nel formato di salvataggio specificato, producendo modifiche come un numero di revisioni di modifica e formato.

```csharp
public static void Compare(Stream v1, Stream v2, Stream outputStream, SaveFormat saveFormat, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| v1 | Stream | Il documento originale. |
| v2 | Stream | Il documento modificato. |
| outputStream | Stream | Il flusso di output. |
| saveFormat | SaveFormat | Formato di salvataggio dell'output. |
| author | String | Iniziali dell'autore da utilizzare per le revisioni. |
| dateTime | DateTime | Data e ora da utilizzare per le revisioni. |
| compareOptions | CompareOptions | Opzioni di confronto dei documenti. |

## Osservazioni

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la prima pagina dell'output verrà salvata nel flusso specificato.

Se il formato di output è TIFF, l'output verrà salvato come un singolo TIFF multi-frame nel flusso specificato.

## Esempi

Mostra come confrontare i documenti dal flusso.

```csharp
// Esistono diversi modi per confrontare i documenti dal flusso:
using (FileStream firstStreamIn = new FileStream(MyDir + "Table column bookmarks.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Table column bookmarks.doc", FileMode.Open, FileAccess.Read))
    {
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.CompareStreamDocuments.1.docx", FileMode.Create, FileAccess.ReadWrite))
            Comparer.Compare(firstStreamIn, secondStreamIn, streamOut, SaveFormat.Docx, "Author", new DateTime());

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.CompareStreamDocuments.2.docx", FileMode.Create, FileAccess.ReadWrite))
        {
            CompareOptions compareOptions = new CompareOptions();
            compareOptions.IgnoreCaseChanges = true;
            Comparer.Compare(firstStreamIn, secondStreamIn, streamOut, SaveFormat.Docx, "Author", new DateTime(), compareOptions);
        }
    }
}
```

### Guarda anche

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## Compare(*Stream, Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#compare_1}

Confronta due documenti caricati da flussi con opzioni aggiuntive e salva le differenze nel flusso di output fornito nel formato di salvataggio specificato, producendo modifiche come un numero di revisioni di modifica e formato.

```csharp
public static void Compare(Stream v1, Stream v2, Stream outputStream, SaveOptions saveOptions, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| v1 | Stream | Il documento originale. |
| v2 | Stream | Il documento modificato. |
| outputStream | Stream | Il flusso di output. |
| saveOptions | SaveOptions | Opzioni di salvataggio dell'output. |
| author | String | Iniziali dell'autore da utilizzare per le revisioni. |
| dateTime | DateTime | Data e ora da utilizzare per le revisioni. |
| compareOptions | CompareOptions | Opzioni di confronto dei documenti. |

## Osservazioni

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la prima pagina dell'output verrà salvata nel flusso specificato.

Se il formato di output è TIFF, l'output verrà salvato come un singolo TIFF multi-frame nel flusso specificato.

### Guarda anche

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)
