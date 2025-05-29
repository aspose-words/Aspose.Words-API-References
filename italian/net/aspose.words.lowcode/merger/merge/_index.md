---
title: Merger.Merge
linktitle: Merge
articleTitle: Merge
second_title: Aspose.Words per .NET
description: Combina senza sforzo più documenti in uno solo con il nostro metodo Merger Merge. Semplifica il tuo flusso di lavoro con opzioni di file personalizzabili oggi stesso!
type: docs
weight: 20
url: /it/net/aspose.words.lowcode/merger/merge/
---
## Merge(*string, string[]*) {#merge_8}

Unisce i documenti di input specificati in un singolo documento di output utilizzando input e nomi di file di output specificati utilizzandoKeepSourceFormatting .

```csharp
public static void Merge(string outputFile, string[] inputFiles)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| outputFile | String | Nome del file di output. |
| inputFiles | String[] | nomi dei file di input. |

## Osservazioni

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà utilizzato per generare i nomi file per ogni parte, seguendo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un singolo file TIFF multi-frame.

## Esempi

Mostra come unire i documenti in un unico documento di output.

```csharp
//Esistono diversi modi per unire i documenti:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.1.docx", new[] { inputDoc1, inputDoc2 });

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.2.docx", new[] { inputDoc1, inputDoc2 }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.3.pdf", new[] { inputDoc1, inputDoc2 }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.4.docx", new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Document doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.5.docx");

doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.6.docx");
```

### Guarda anche

* class [Merger](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## Merge(*string, string[], [SaveFormat](../../../aspose.words/saveformat/), [MergeFormatMode](../../mergeformatmode/)*) {#merge_10}

Unisce i documenti di input specificati in un singolo documento di output utilizzando i nomi dei file di input e output specificati e il formato del documento finale.

```csharp
public static void Merge(string outputFile, string[] inputFiles, SaveFormat saveFormat, 
    MergeFormatMode mergeFormatMode)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| outputFile | String | Nome del file di output. |
| inputFiles | String[] | nomi dei file di input. |
| saveFormat | SaveFormat | Formato di salvataggio. |
| mergeFormatMode | MergeFormatMode | Specifica come unire la formattazione in conflitto. |

## Osservazioni

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà utilizzato per generare i nomi file per ogni parte, seguendo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un singolo file TIFF multi-frame.

## Esempi

Mostra come unire i documenti in un unico documento di output.

```csharp
//Esistono diversi modi per unire i documenti:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.1.docx", new[] { inputDoc1, inputDoc2 });

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.2.docx", new[] { inputDoc1, inputDoc2 }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.3.pdf", new[] { inputDoc1, inputDoc2 }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.4.docx", new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Document doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.5.docx");

doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.6.docx");
```

### Guarda anche

* enum [SaveFormat](../../../aspose.words/saveformat/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## Merge(*string, string[], [SaveOptions](../../../aspose.words.saving/saveoptions/), [MergeFormatMode](../../mergeformatmode/)*) {#merge_11}

Unisce i documenti di input specificati in un singolo documento di output utilizzando i nomi dei file di input e output specificati e le opzioni di salvataggio.

```csharp
public static void Merge(string outputFile, string[] inputFiles, SaveOptions saveOptions, 
    MergeFormatMode mergeFormatMode)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| outputFile | String | Nome del file di output. |
| inputFiles | String[] | nomi dei file di input. |
| saveOptions | SaveOptions | Le opzioni di salvataggio. |
| mergeFormatMode | MergeFormatMode | Specifica come unire la formattazione in conflitto. |

## Osservazioni

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà utilizzato per generare i nomi file per ogni parte, seguendo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un singolo file TIFF multi-frame.

## Esempi

Mostra come unire i documenti in un unico documento di output.

```csharp
//Esistono diversi modi per unire i documenti:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.1.docx", new[] { inputDoc1, inputDoc2 });

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.2.docx", new[] { inputDoc1, inputDoc2 }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.3.pdf", new[] { inputDoc1, inputDoc2 }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.4.docx", new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Document doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.5.docx");

doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.6.docx");
```

### Guarda anche

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## Merge(*string, string[], LoadOptions[], [SaveOptions](../../../aspose.words.saving/saveoptions/), [MergeFormatMode](../../mergeformatmode/)*) {#merge_9}

Unisce i documenti di input specificati in un singolo documento di output utilizzando i nomi dei file di input e output specificati e le opzioni di salvataggio.

```csharp
public static void Merge(string outputFile, string[] inputFiles, LoadOptions[] loadOptions, 
    SaveOptions saveOptions, MergeFormatMode mergeFormatMode)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| outputFile | String | Nome del file di output. |
| inputFiles | String[] | nomi dei file di input. |
| loadOptions | LoadOptions[] | Opzioni di caricamento per i file di input. |
| saveOptions | SaveOptions | Le opzioni di salvataggio. |
| mergeFormatMode | MergeFormatMode | Specifica come unire la formattazione in conflitto. |

## Osservazioni

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà utilizzato per generare i nomi file per ogni parte, seguendo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un singolo file TIFF multi-frame.

## Esempi

Mostra come unire i documenti in un unico documento di output.

```csharp
//Esistono diversi modi per unire i documenti:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.1.docx", new[] { inputDoc1, inputDoc2 });

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.2.docx", new[] { inputDoc1, inputDoc2 }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.3.pdf", new[] { inputDoc1, inputDoc2 }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.4.docx", new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Document doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.5.docx");

doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.6.docx");
```

### Guarda anche

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## Merge(*string[], [MergeFormatMode](../../mergeformatmode/)*) {#merge_4}

Unisce i documenti di input specificati in un unico documento e restituisce[`Document`](../../../aspose.words/document/) istanza del documento finale.

```csharp
public static Document Merge(string[] inputFiles, MergeFormatMode mergeFormatMode)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFiles | String[] | nomi dei file di input. |
| mergeFormatMode | MergeFormatMode | Specifica come unire la formattazione in conflitto. |

## Esempi

Mostra come unire i documenti in un unico documento di output.

```csharp
//Esistono diversi modi per unire i documenti:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.1.docx", new[] { inputDoc1, inputDoc2 });

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.2.docx", new[] { inputDoc1, inputDoc2 }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.3.pdf", new[] { inputDoc1, inputDoc2 }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.4.docx", new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Document doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.5.docx");

doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.6.docx");
```

### Guarda anche

* class [Document](../../../aspose.words/document/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## Merge(*string[], LoadOptions[], [MergeFormatMode](../../mergeformatmode/)*) {#merge_3}

Unisce i documenti di input specificati in un unico documento e restituisce[`Document`](../../../aspose.words/document/) istanza del documento finale.

```csharp
public static Document Merge(string[] inputFiles, LoadOptions[] loadOptions, 
    MergeFormatMode mergeFormatMode)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFiles | String[] | nomi dei file di input. |
| loadOptions | LoadOptions[] | Opzioni di caricamento per i file di input. |
| mergeFormatMode | MergeFormatMode | Specifica come unire la formattazione in conflitto. |

## Esempi

Mostra come unire i documenti in un unico documento di output.

```csharp
//Esistono diversi modi per unire i documenti:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.1.docx", new[] { inputDoc1, inputDoc2 });

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.2.docx", new[] { inputDoc1, inputDoc2 }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.3.pdf", new[] { inputDoc1, inputDoc2 }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.4.docx", new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Document doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.5.docx");

doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.6.docx");
```

### Guarda anche

* class [Document](../../../aspose.words/document/)
* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## Merge(*Document[], [MergeFormatMode](../../mergeformatmode/)*) {#merge}

Unisce i documenti di input specificati in un unico documento e restituisce[`Document`](../../../aspose.words/document/) istanza del documento finale.

```csharp
public static Document Merge(Document[] inputDocuments, MergeFormatMode mergeFormatMode)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputDocuments | Document[] | I documenti di input. |
| mergeFormatMode | MergeFormatMode | Specifica come unire la formattazione in conflitto. |

## Esempi

Mostra come unire documenti di input in un'unica istanza di documento.

```csharp
DocumentBuilder firstDoc = new DocumentBuilder();
firstDoc.Font.Size = 16;
firstDoc.Font.Color = Color.Blue;
firstDoc.Write("Hello first word!");

DocumentBuilder secondDoc = new DocumentBuilder();
secondDoc.Write("Hello second word!");

Document mergedDoc = Merger.Merge(new Document[] { firstDoc.Document, secondDoc.Document }, MergeFormatMode.KeepSourceLayout);
Assert.AreEqual("Hello first word!\fHello second word!\f", mergedDoc.GetText());
```

### Guarda anche

* class [Document](../../../aspose.words/document/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## Merge(*Stream, Stream[], [SaveFormat](../../../aspose.words/saveformat/)*) {#merge_6}

Unisce i documenti di input specificati in un singolo documento di output utilizzando i flussi di input e output specificati e il formato del documento finale.

```csharp
public static void Merge(Stream outputStream, Stream[] inputStreams, SaveFormat saveFormat)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| outputStream | Stream | Il flusso di output. |
| inputStreams | Stream[] | I flussi di input. |
| saveFormat | SaveFormat | Formato di salvataggio. |

## Osservazioni

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la prima pagina dell'output verrà salvata nel flusso specificato.

Se il formato di output è TIFF, l'output verrà salvato come un singolo TIFF multi-frame nel flusso specificato.

## Esempi

Mostra come unire i documenti del flusso in un unico documento di output.

```csharp
//Esistono diversi modi per unire i documenti dal flusso:
using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.1.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, saveOptions, MergeFormatMode.KeepSourceFormatting);

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.2.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, SaveFormat.Docx);

        LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
        LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.3.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

        Document firstDoc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, MergeFormatMode.MergeFormatting);
        firstDoc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.4.docx");

        Document secondDoc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
        secondDoc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.5.docx");
    }
}
```

### Guarda anche

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Merger](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## Merge(*Stream, Stream[], [SaveOptions](../../../aspose.words.saving/saveoptions/), [MergeFormatMode](../../mergeformatmode/)*) {#merge_7}

Unisce i documenti di input specificati in un singolo documento di output utilizzando flussi di input e output specificati e opzioni di salvataggio.

```csharp
public static void Merge(Stream outputStream, Stream[] inputStreams, SaveOptions saveOptions, 
    MergeFormatMode mergeFormatMode)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| outputStream | Stream | Il flusso di output. |
| inputStreams | Stream[] | I flussi di input. |
| saveOptions | SaveOptions | Le opzioni di salvataggio. |
| mergeFormatMode | MergeFormatMode | Specifica come unire la formattazione in conflitto. |

## Osservazioni

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la prima pagina dell'output verrà salvata nel flusso specificato.

Se il formato di output è TIFF, l'output verrà salvato come un singolo TIFF multi-frame nel flusso specificato.

## Esempi

Mostra come unire i documenti del flusso in un unico documento di output.

```csharp
//Esistono diversi modi per unire i documenti dal flusso:
using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.1.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, saveOptions, MergeFormatMode.KeepSourceFormatting);

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.2.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, SaveFormat.Docx);

        LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
        LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.3.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

        Document firstDoc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, MergeFormatMode.MergeFormatting);
        firstDoc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.4.docx");

        Document secondDoc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
        secondDoc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.5.docx");
    }
}
```

### Guarda anche

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## Merge(*Stream, Stream[], LoadOptions[], [SaveOptions](../../../aspose.words.saving/saveoptions/), [MergeFormatMode](../../mergeformatmode/)*) {#merge_5}

Unisce i documenti di input specificati in un singolo documento di output utilizzando flussi di input e output specificati e opzioni di salvataggio.

```csharp
public static void Merge(Stream outputStream, Stream[] inputStreams, LoadOptions[] loadOptions, 
    SaveOptions saveOptions, MergeFormatMode mergeFormatMode)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| outputStream | Stream | Il flusso di output. |
| inputStreams | Stream[] | I flussi di input. |
| loadOptions | LoadOptions[] | Opzioni di caricamento per i file di input. |
| saveOptions | SaveOptions | Le opzioni di salvataggio. |
| mergeFormatMode | MergeFormatMode | Specifica come unire la formattazione in conflitto. |

## Osservazioni

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la prima pagina dell'output verrà salvata nel flusso specificato.

Se il formato di output è TIFF, l'output verrà salvato come un singolo TIFF multi-frame nel flusso specificato.

## Esempi

Mostra come unire i documenti del flusso in un unico documento di output.

```csharp
//Esistono diversi modi per unire i documenti dal flusso:
using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.1.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, saveOptions, MergeFormatMode.KeepSourceFormatting);

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.2.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, SaveFormat.Docx);

        LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
        LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.3.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

        Document firstDoc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, MergeFormatMode.MergeFormatting);
        firstDoc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.4.docx");

        Document secondDoc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
        secondDoc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.5.docx");
    }
}
```

### Guarda anche

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## Merge(*Stream[], [MergeFormatMode](../../mergeformatmode/)*) {#merge_2}

Unisce i documenti di input specificati in un unico documento e restituisce[`Document`](../../../aspose.words/document/) istanza del documento finale.

```csharp
public static Document Merge(Stream[] inputStreams, MergeFormatMode mergeFormatMode)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStreams | Stream[] | I flussi di input. |
| mergeFormatMode | MergeFormatMode | Specifica come unire la formattazione in conflitto. |

## Esempi

Mostra come unire i documenti del flusso in un unico documento di output.

```csharp
//Esistono diversi modi per unire i documenti dal flusso:
using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.1.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, saveOptions, MergeFormatMode.KeepSourceFormatting);

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.2.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, SaveFormat.Docx);

        LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
        LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.3.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

        Document firstDoc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, MergeFormatMode.MergeFormatting);
        firstDoc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.4.docx");

        Document secondDoc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
        secondDoc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.5.docx");
    }
}
```

### Guarda anche

* class [Document](../../../aspose.words/document/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## Merge(*Stream[], LoadOptions[], [MergeFormatMode](../../mergeformatmode/)*) {#merge_1}

Unisce i documenti di input specificati in un unico documento e restituisce[`Document`](../../../aspose.words/document/) istanza del documento finale.

```csharp
public static Document Merge(Stream[] inputStreams, LoadOptions[] loadOptions, 
    MergeFormatMode mergeFormatMode)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStreams | Stream[] | I flussi di input. |
| loadOptions | LoadOptions[] | Opzioni di caricamento per i file di input. |
| mergeFormatMode | MergeFormatMode | Specifica come unire la formattazione in conflitto. |

## Esempi

Mostra come unire i documenti del flusso in un unico documento di output.

```csharp
//Esistono diversi modi per unire i documenti dal flusso:
using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.1.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, saveOptions, MergeFormatMode.KeepSourceFormatting);

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.2.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, SaveFormat.Docx);

        LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
        LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.3.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

        Document firstDoc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, MergeFormatMode.MergeFormatting);
        firstDoc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.4.docx");

        Document secondDoc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
        secondDoc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.5.docx");
    }
}
```

### Guarda anche

* class [Document](../../../aspose.words/document/)
* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)
