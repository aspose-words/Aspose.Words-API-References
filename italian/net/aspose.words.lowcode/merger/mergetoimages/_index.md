---
title: Merger.MergeToImages
linktitle: MergeToImages
articleTitle: MergeToImages
second_title: Aspose.Words per .NET
description: Unisci più documenti senza sforzo con il metodo MergeToImages, creando un'unica immagine in output e personalizzando i nomi dei file e le opzioni di salvataggio.
type: docs
weight: 30
url: /it/net/aspose.words.lowcode/merger/mergetoimages/
---
## MergeToImages(*string[], [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), [MergeFormatMode](../../mergeformatmode/)*) {#mergetoimages_1}

Unisce i documenti di input specificati in un singolo documento di output utilizzando i nomi dei file di input e output specificati e le opzioni di salvataggio. Esegue il rendering dell'output in immagini.

```csharp
public static Stream[] MergeToImages(string[] inputFiles, ImageSaveOptions saveOptions, 
    MergeFormatMode mergeFormatMode)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFiles | String[] | nomi dei file di input. |
| saveOptions | ImageSaveOptions | Le opzioni di salvataggio. |
| mergeFormatMode | MergeFormatMode | Specifica come unire la formattazione in conflitto. |

### Guarda anche

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## MergeToImages(*Stream[], [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), [MergeFormatMode](../../mergeformatmode/)*) {#mergetoimages}

Unisce i flussi di documenti di input specificati in un singolo documento di output utilizzando le opzioni di salvataggio delle immagini specificate. Esegue il rendering dell'output in immagini.

```csharp
public static Stream[] MergeToImages(Stream[] inputStreams, ImageSaveOptions saveOptions, 
    MergeFormatMode mergeFormatMode)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStreams | Stream[] | Il file di input viene trasmesso in streaming. |
| saveOptions | ImageSaveOptions | Le opzioni di salvataggio. |
| mergeFormatMode | MergeFormatMode | Specifica come unire la formattazione in conflitto. |

### Guarda anche

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)
