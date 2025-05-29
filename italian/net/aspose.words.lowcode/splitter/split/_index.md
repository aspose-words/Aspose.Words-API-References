---
title: Splitter.Split
linktitle: Split
articleTitle: Split
second_title: Aspose.Words per .NET
description: Dividi facilmente i documenti in più sezioni con il nostro flessibile metodo Splitter Split. Salva nel tuo formato preferito per una facile gestione dei file!
type: docs
weight: 40
url: /it/net/aspose.words.lowcode/splitter/split/
---
## Split(*string, string, [SplitOptions](../../splitoptions/)*) {#split_2}

Divide un documento in più parti in base alle opzioni di divisione specificate e salva le parti risultanti in file. Il formato del file di output è determinato dall'estensione del nome del file di output.

```csharp
public static void Split(string inputFileName, string outputFileName, SplitOptions options)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | String | Nome del file di input. |
| outputFileName | String | Nome del file di output utilizzato per generare il nome del file per le parti del documento utilizzando la regola "outputFile_partIndex.extension" |
| options | SplitOptions | Opzioni di suddivisione del documento. |

## Esempi

Mostra come dividere un documento in base alle pagine.

```csharp
string doc = MyDir + "Big document.docx";

SplitOptions options = new SplitOptions();
options.SplitCriteria = SplitCriteria.Page;
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.1.docx", options);
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.2.docx", SaveFormat.Docx, options);
```

### Guarda anche

* class [SplitOptions](../../splitoptions/)
* class [Splitter](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## Split(*string, string, [SaveFormat](../../../aspose.words/saveformat/), [SplitOptions](../../splitoptions/)*) {#split_3}

Divide un documento in più parti in base alle opzioni di divisione specificate e salva le parti risultanti in file nel formato di salvataggio specificato.

```csharp
public static void Split(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    SplitOptions options)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | String | Nome del file di input. |
| outputFileName | String | Nome del file di output utilizzato per generare il nome del file per le parti del documento utilizzando la regola "outputFile_partIndex.extension" |
| saveFormat | SaveFormat | Formato di salvataggio. |
| options | SplitOptions | Opzioni di suddivisione del documento. |

## Esempi

Mostra come dividere un documento in base alle pagine.

```csharp
string doc = MyDir + "Big document.docx";

SplitOptions options = new SplitOptions();
options.SplitCriteria = SplitCriteria.Page;
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.1.docx", options);
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.2.docx", SaveFormat.Docx, options);
```

### Guarda anche

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [SplitOptions](../../splitoptions/)
* class [Splitter](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## Split(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), [SplitOptions](../../splitoptions/)*) {#split_4}

Divide un documento in più parti in base alle opzioni di divisione specificate e salva le parti risultanti in file nel formato di salvataggio specificato.

```csharp
public static void Split(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    SplitOptions options)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | String | Nome del file di input. |
| outputFileName | String | Nome del file di output utilizzato per generare il nome del file per le parti del documento utilizzando la regola "outputFile_partIndex.extension" |
| saveOptions | SaveOptions | Le opzioni di salvataggio. |
| options | SplitOptions | Opzioni di suddivisione del documento. |

### Guarda anche

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [SplitOptions](../../splitoptions/)
* class [Splitter](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## Split(*Stream, [SaveFormat](../../../aspose.words/saveformat/), [SplitOptions](../../splitoptions/)*) {#split}

Divide un documento da un flusso di input in più parti in base alle opzioni di divisione specificate e restituisce le parti risultanti come una matrice di flussi nel formato di salvataggio specificato.

```csharp
public static Stream[] Split(Stream inputStream, SaveFormat saveFormat, SplitOptions options)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | Stream | Il flusso di input. |
| saveFormat | SaveFormat | Formato di salvataggio. |
| options | SplitOptions | Opzioni di suddivisione del documento. |

## Esempi

Mostra come suddividere un documento dal flusso in base alle pagine.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    SplitOptions options = new SplitOptions();
    options.SplitCriteria = SplitCriteria.Page;
    Stream[] stream = Splitter.Split(streamIn, SaveFormat.Docx, options);
}
```

### Guarda anche

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [SplitOptions](../../splitoptions/)
* class [Splitter](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## Split(*Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), [SplitOptions](../../splitoptions/)*) {#split_1}

Divide un documento da un flusso di input in più parti in base alle opzioni di divisione specificate e restituisce le parti risultanti come una matrice di flussi nel formato di salvataggio specificato.

```csharp
public static Stream[] Split(Stream inputStream, SaveOptions saveOptions, SplitOptions options)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | Stream | Il flusso di input. |
| saveOptions | SaveOptions | Le opzioni di salvataggio. |
| options | SplitOptions | Opzioni di suddivisione del documento. |

### Guarda anche

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [SplitOptions](../../splitoptions/)
* class [Splitter](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)
