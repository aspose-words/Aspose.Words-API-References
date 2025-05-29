---
title: Splitter.RemoveBlankPages
linktitle: RemoveBlankPages
articleTitle: RemoveBlankPages
second_title: Aspose.Words per .NET
description: Elimina senza sforzo le pagine vuote dai tuoi documenti con il metodo RemoveBlankPages di Splitter. Risparmia tempo e migliora il tuo flusso di lavoro oggi stesso!
type: docs
weight: 30
url: /it/net/aspose.words.lowcode/splitter/removeblankpages/
---
## RemoveBlankPages(*string, string*) {#removeblankpages_2}

Rimuove le pagine vuote dal documento e salva l'output. Restituisce un elenco dei numeri di pagina rimossi.

```csharp
public static List<int> RemoveBlankPages(string inputFileName, string outputFileName)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | String | Nome del file di input. |
| outputFileName | String | Nome del file di output. |

### Valore di ritorno

L'elenco dei numeri di pagina è stato considerato vuoto e rimosso.

## Esempi

Mostra come rimuovere le pagine vuote dal documento.

```csharp
// Esistono diversi modi per rimuovere le pagine vuote dal documento:
string doc = MyDir + "Blank pages.docx";

Splitter.RemoveBlankPages(doc, ArtifactsDir + "LowCode.RemoveBlankPages.1.docx");
Splitter.RemoveBlankPages(doc, ArtifactsDir + "LowCode.RemoveBlankPages.2.docx", SaveFormat.Docx);
```

### Guarda anche

* class [Splitter](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## RemoveBlankPages(*string, string, [SaveFormat](../../../aspose.words/saveformat/)*) {#removeblankpages_3}

Rimuove le pagine vuote dal documento e salva l'output nel formato specificato. Restituisce un elenco dei numeri di pagina rimossi.

```csharp
public static List<int> RemoveBlankPages(string inputFileName, string outputFileName, 
    SaveFormat saveFormat)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | String | Nome del file di input. |
| outputFileName | String | Nome del file di output. |
| saveFormat | SaveFormat | Formato di salvataggio. |

### Valore di ritorno

L'elenco dei numeri di pagina è stato considerato vuoto e rimosso.

## Esempi

Mostra come rimuovere le pagine vuote dal documento.

```csharp
// Esistono diversi modi per rimuovere le pagine vuote dal documento:
string doc = MyDir + "Blank pages.docx";

Splitter.RemoveBlankPages(doc, ArtifactsDir + "LowCode.RemoveBlankPages.1.docx");
Splitter.RemoveBlankPages(doc, ArtifactsDir + "LowCode.RemoveBlankPages.2.docx", SaveFormat.Docx);
```

### Guarda anche

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Splitter](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## RemoveBlankPages(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#removeblankpages_4}

Rimuove le pagine vuote dal documento e salva l'output nel formato specificato. Restituisce un elenco dei numeri di pagina rimossi.

```csharp
public static List<int> RemoveBlankPages(string inputFileName, string outputFileName, 
    SaveOptions saveOptions)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | String | Nome del file di input. |
| outputFileName | String | Nome del file di output. |
| saveOptions | SaveOptions | Le opzioni di salvataggio. |

### Valore di ritorno

L'elenco dei numeri di pagina è stato considerato vuoto e rimosso.

### Guarda anche

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Splitter](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## RemoveBlankPages(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/)*) {#removeblankpages}

Rimuove le pagine vuote da un documento fornito in un flusso di input e salva il documento aggiornato in un flusso di output nel formato di salvataggio specificato. Restituisce un elenco dei numeri di pagina rimossi.

```csharp
public static List<int> RemoveBlankPages(Stream inputStream, Stream outputStream, 
    SaveFormat saveFormat)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | Stream | Il flusso di input. |
| outputStream | Stream | Il flusso di output. |
| saveFormat | SaveFormat | Formato di salvataggio. |

### Valore di ritorno

L'elenco dei numeri di pagina è stato considerato vuoto e rimosso.

## Esempi

Mostra come rimuovere le pagine vuote dal documento nel flusso.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Blank pages.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.RemoveBlankPagesStream.docx", FileMode.Create, FileAccess.ReadWrite))
        Splitter.RemoveBlankPages(streamIn, streamOut, SaveFormat.Docx);
}
```

### Guarda anche

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Splitter](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## RemoveBlankPages(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#removeblankpages_1}

Rimuove le pagine vuote da un documento fornito in un flusso di input e salva il documento aggiornato in un flusso di output nel formato di salvataggio specificato. Restituisce un elenco dei numeri di pagina rimossi.

```csharp
public static List<int> RemoveBlankPages(Stream inputStream, Stream outputStream, 
    SaveOptions saveOptions)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | Stream | Il flusso di input. |
| outputStream | Stream | Il flusso di output. |
| saveOptions | SaveOptions | Le opzioni di salvataggio. |

### Valore di ritorno

L'elenco dei numeri di pagina è stato considerato vuoto e rimosso.

### Guarda anche

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Splitter](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)
