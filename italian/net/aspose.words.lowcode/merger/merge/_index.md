---
title: Merger.Merge
second_title: Aspose.Words per .NET API Reference
description: Merger metodo. Unisce i documenti di input specificati in un singolo documento di output utilizzando i nomi di file di input e output specificati.
type: docs
weight: 10
url: /it/net/aspose.words.lowcode/merger/merge/
---
## Merge(string, string[]) {#merge_4}

Unisce i documenti di input specificati in un singolo documento di output utilizzando i nomi di file di input e output specificati.

```csharp
public static void Merge(string outputFile, string[] inputFiles)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| outputFile | String | Il nome del file di output. |
| inputFiles | String[] | I nomi dei file di input. |

### Osservazioni

Per impostazione predefinitaKeepSourceFormatting si usa.

### Esempi

Mostra come unire i documenti in un unico documento di output.

```csharp
//Esistono diversi modi per unire i documenti:
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SimpleMerge.docx", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" });

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SaveOptions.docx", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, new OoxmlSaveOptions() { Password = "Aspose.Words" }, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SaveFormat.pdf", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

Document doc = Merger.Merge(new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.DocumentInstance.docx");
```

### Guarda anche

* class [Merger](../)
* spazio dei nomi [Aspose.Words.LowCode](../../merger/)
* assemblea [Aspose.Words](../../../)

---

## Merge(string, string[], SaveFormat, MergeFormatMode) {#merge_5}

Unisce i documenti di input specificati in un singolo documento di output utilizzando i nomi dei file di input e output specificati e il formato del documento finale.

```csharp
public static void Merge(string outputFile, string[] inputFiles, SaveFormat saveFormat, 
    MergeFormatMode mergeFormatMode)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| outputFile | String | Il nome del file di output. |
| inputFiles | String[] | I nomi dei file di input. |
| saveFormat | SaveFormat | Il formato di salvataggio. |
| mergeFormatMode | MergeFormatMode | Specifica come unire la formattazione in conflitto. |

### Esempi

Mostra come unire i documenti in un unico documento di output.

```csharp
//Esistono diversi modi per unire i documenti:
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SimpleMerge.docx", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" });

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SaveOptions.docx", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, new OoxmlSaveOptions() { Password = "Aspose.Words" }, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SaveFormat.pdf", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

Document doc = Merger.Merge(new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.DocumentInstance.docx");
```

### Guarda anche

* enum [SaveFormat](../../../aspose.words/saveformat/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* spazio dei nomi [Aspose.Words.LowCode](../../merger/)
* assemblea [Aspose.Words](../../../)

---

## Merge(string, string[], SaveOptions, MergeFormatMode) {#merge_6}

Unisce i documenti di input specificati in un singolo documento di output utilizzando i nomi dei file di input e di output specificati e le opzioni di salvataggio.

```csharp
public static void Merge(string outputFile, string[] inputFiles, SaveOptions saveOptions, 
    MergeFormatMode mergeFormatMode)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| outputFile | String | Il nome del file di output. |
| inputFiles | String[] | I nomi dei file di input. |
| saveOptions | SaveOptions | Le opzioni di salvataggio. |
| mergeFormatMode | MergeFormatMode | Specifica come unire la formattazione in conflitto. |

### Esempi

Mostra come unire i documenti in un unico documento di output.

```csharp
//Esistono diversi modi per unire i documenti:
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SimpleMerge.docx", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" });

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SaveOptions.docx", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, new OoxmlSaveOptions() { Password = "Aspose.Words" }, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SaveFormat.pdf", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

Document doc = Merger.Merge(new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.DocumentInstance.docx");
```

### Guarda anche

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* spazio dei nomi [Aspose.Words.LowCode](../../merger/)
* assemblea [Aspose.Words](../../../)

---

## Merge(string[], MergeFormatMode) {#merge_1}

Unisce i documenti di input specificati in un unico documento e restituisce[`Document`](../../../aspose.words/document/) istanza del documento finale.

```csharp
public static Document Merge(string[] inputFiles, MergeFormatMode mergeFormatMode)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFiles | String[] | I nomi dei file di input. |
| mergeFormatMode | MergeFormatMode | Specifica come unire la formattazione in conflitto. |

### Esempi

Mostra come unire i documenti in un unico documento di output.

```csharp
//Esistono diversi modi per unire i documenti:
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SimpleMerge.docx", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" });

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SaveOptions.docx", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, new OoxmlSaveOptions() { Password = "Aspose.Words" }, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SaveFormat.pdf", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

Document doc = Merger.Merge(new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.DocumentInstance.docx");
```

### Guarda anche

* class [Document](../../../aspose.words/document/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* spazio dei nomi [Aspose.Words.LowCode](../../merger/)
* assemblea [Aspose.Words](../../../)

---

## Merge(Stream, Stream[], SaveFormat) {#merge_2}

Unisce i documenti di input specificati in un singolo documento di output utilizzando i flussi di input e output specificati e il formato del documento finale.

```csharp
public static void Merge(Stream outputStream, Stream[] inputStreams, SaveFormat saveFormat)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| outputStream | Stream | Il flusso di output. |
| inputStreams | Stream[] | I flussi di input. |
| saveFormat | SaveFormat | Il formato di salvataggio. |

### Esempi

Mostra come unire i documenti dallo stream in un unico documento di output.

```csharp
//Esistono diversi modi per unire i documenti dallo stream:
using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.SaveOptions.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, new OoxmlSaveOptions() { Password = "Aspose.Words" }, MergeFormatMode.KeepSourceFormatting);

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.SaveFormat.docx", FileMode.Create, FileAccess.ReadWrite))                    
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, SaveFormat.Docx);

        Document doc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, MergeFormatMode.MergeFormatting);
        doc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.DocumentInstance.docx");
    }
}
```

### Guarda anche

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Merger](../)
* spazio dei nomi [Aspose.Words.LowCode](../../merger/)
* assemblea [Aspose.Words](../../../)

---

## Merge(Stream, Stream[], SaveOptions, MergeFormatMode) {#merge_3}

Unisce i documenti di input specificati in un singolo documento di output utilizzando i flussi di input e output specificati e le opzioni di salvataggio.

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

### Esempi

Mostra come unire i documenti dallo stream in un unico documento di output.

```csharp
//Esistono diversi modi per unire i documenti dallo stream:
using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.SaveOptions.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, new OoxmlSaveOptions() { Password = "Aspose.Words" }, MergeFormatMode.KeepSourceFormatting);

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.SaveFormat.docx", FileMode.Create, FileAccess.ReadWrite))                    
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, SaveFormat.Docx);

        Document doc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, MergeFormatMode.MergeFormatting);
        doc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.DocumentInstance.docx");
    }
}
```

### Guarda anche

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* spazio dei nomi [Aspose.Words.LowCode](../../merger/)
* assemblea [Aspose.Words](../../../)

---

## Merge(Stream[], MergeFormatMode) {#merge}

Unisce i documenti di input specificati in un unico documento e restituisce[`Document`](../../../aspose.words/document/) istanza del documento finale.

```csharp
public static Document Merge(Stream[] inputStreams, MergeFormatMode mergeFormatMode)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStreams | Stream[] | I flussi di input. |
| mergeFormatMode | MergeFormatMode | Specifica come unire la formattazione in conflitto. |

### Esempi

Mostra come unire i documenti dallo stream in un unico documento di output.

```csharp
//Esistono diversi modi per unire i documenti dallo stream:
using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.SaveOptions.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, new OoxmlSaveOptions() { Password = "Aspose.Words" }, MergeFormatMode.KeepSourceFormatting);

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.SaveFormat.docx", FileMode.Create, FileAccess.ReadWrite))                    
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, SaveFormat.Docx);

        Document doc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, MergeFormatMode.MergeFormatting);
        doc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.DocumentInstance.docx");
    }
}
```

### Guarda anche

* class [Document](../../../aspose.words/document/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* spazio dei nomi [Aspose.Words.LowCode](../../merger/)
* assemblea [Aspose.Words](../../../)


