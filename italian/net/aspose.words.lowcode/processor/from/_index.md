---
title: Processor.From
linktitle: From
articleTitle: From
second_title: Aspose.Words per .NET
description: Migliora il tuo flusso di lavoro con il nostro processore che gestisce in modo efficiente i documenti in ingresso, garantendo un'elaborazione fluida e una maggiore produttività.
type: docs
weight: 20
url: /it/net/aspose.words.lowcode/processor/from/
---
## From(*string, [LoadOptions](../../../aspose.words.loading/loadoptions/)*) {#from_1}

Specifica il documento di input per l'elaborazione.

```csharp
public Processor From(string input, LoadOptions loadOptions = null)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| input | String | Nome del file del documento di input. |
| loadOptions | LoadOptions | Opzioni di caricamento facoltative utilizzate per caricare il documento. |

### Valore di ritorno

Restituisce il processore con il file di input specificato.

## Osservazioni

Se il processore accetta un solo file come input, verrà elaborato solo l'ultimo file specificato. [`Merger`](../../merger/) il processore accetta più file come input, come risultato tutti i documenti specificati verranno uniti. [`Converter`](../../converter/) il processore accetta solo un file come input, quindi verrà convertito solo l'ultimo file specificato.

## Esempi

Mostra come convertire documenti con una singola riga di codice utilizzando il contesto.

```csharp
string doc = MyDir + "Big document.docx";

Converter.Create(new ConverterContext())
    .From(doc)
    .To(ArtifactsDir + "LowCode.ConvertContext.1.pdf")
    .Execute();

Converter.Create(new ConverterContext())
    .From(doc)
    .To(ArtifactsDir + "LowCode.ConvertContext.2.pdf", SaveFormat.Rtf)
    .Execute();

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Converter.Create(new ConverterContext())
    .From(doc, loadOptions)
    .To(ArtifactsDir + "LowCode.ConvertContext.3.docx", saveOptions)
    .Execute();

Converter.Create(new ConverterContext())
    .From(doc)
    .To(ArtifactsDir + "LowCode.ConvertContext.4.png", new ImageSaveOptions(SaveFormat.Png))
    .Execute();
```

Mostra come unire documenti in un unico documento di output utilizzando il contesto.

```csharp
//Esistono diversi modi per unire i documenti:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
    .From(inputDoc1)
    .From(inputDoc2)
    .To(ArtifactsDir + "LowCode.MergeContextDocuments.1.docx")
    .Execute();

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
    .From(inputDoc1, firstLoadOptions)
    .From(inputDoc2, secondLoadOptions)
    .To(ArtifactsDir + "LowCode.MergeContextDocuments.2.docx", SaveFormat.Docx)
    .Execute();

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
    .From(inputDoc1)
    .From(inputDoc2)
    .To(ArtifactsDir + "LowCode.MergeContextDocuments.3.docx", saveOptions)
    .Execute();
```

### Guarda anche

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [Processor](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## From(*Stream, [LoadOptions](../../../aspose.words.loading/loadoptions/)*) {#from}

Specifica il documento di input per l'elaborazione.

```csharp
public Processor From(Stream input, LoadOptions loadOptions = null)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| input | Stream | Flusso di documenti in input. |
| loadOptions | LoadOptions | Opzioni di caricamento facoltative utilizzate per caricare il documento. |

### Valore di ritorno

Restituisce il processore con il flusso di file di input specificato.

## Osservazioni

Se il processore accetta un solo file come input, verrà elaborato solo l'ultimo file specificato. [`Merger`](../../merger/) il processore accetta più file come input, come risultato tutti i documenti specificati verranno uniti. [`Converter`](../../converter/) il processore accetta solo un file come input, quindi verrà convertito solo l'ultimo file specificato.

## Esempi

Mostra come convertire documenti da un flusso con una singola riga di codice utilizzando il contesto.

```csharp
string doc = MyDir + "Document.docx";
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertContextStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Create(new ConverterContext())
            .From(streamIn)
            .To(streamOut, SaveFormat.Rtf)
            .Execute();

    OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertContextStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Create(new ConverterContext())
            .From(streamIn, loadOptions)
            .To(streamOut, saveOptions)
            .Execute();

    List<Stream> pages = new List<Stream>();
    Converter.Create(new ConverterContext())
        .From(doc)
        .To(pages, new ImageSaveOptions(SaveFormat.Png))
        .Execute();
}
```

Mostra come unire i documenti del flusso in un singolo documento di output utilizzando il contesto.

```csharp
//Esistono diversi modi per unire i documenti:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamContextDocuments.1.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
            .From(firstStreamIn)
            .From(secondStreamIn)
            .To(streamOut, saveOptions)
            .Execute();

        LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
        LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamContextDocuments.2.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
            .From(firstStreamIn, firstLoadOptions)
            .From(secondStreamIn, secondLoadOptions)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
    }
}
```

### Guarda anche

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [Processor](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)
