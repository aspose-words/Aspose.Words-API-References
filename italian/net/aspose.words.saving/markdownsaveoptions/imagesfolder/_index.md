---
title: ImagesFolder
second_title: Aspose.Words per .NET API Reference
description: Specifica la cartella fisica in cui vengono salvate le immagini durante lesportazione di un documento in Markdown formato. Limpostazione predefinita è una stringa vuota.
type: docs
weight: 40
url: /it/net/aspose.words.saving/markdownsaveoptions/imagesfolder/
---
## MarkdownSaveOptions.ImagesFolder property

Specifica la cartella fisica in cui vengono salvate le immagini durante l'esportazione di un documento in Markdown formato. L'impostazione predefinita è una stringa vuota.

```csharp
public string ImagesFolder { get; set; }
```

### Osservazioni

Quando salvi a[`Document`](../../../aspose.words/document) inMarkdown format, Aspose.Words deve salvare tutte le immagini incorporate nel documento come file standalone. `ImagesFolder` consente di specificare dove verranno salvate le immagini.

Se si salva un documento in un file e si fornisce un nome file, Aspose.Words, per impostazione predefinita, salva le immagini in la stessa cartella in cui è salvato il file del documento. Uso`ImagesFolder` per ignorare questo comportamento.

Se salvi un documento in un flusso, Aspose.Words non ha una cartella dove salvare le immagini, ma deve comunque salvare le immagini da qualche parte. In questo caso, è necessario specificare una cartella accessibile nel file`ImagesFolder` proprietà.

Se la cartella specificata da`ImagesFolder` non esiste, verrà creato automaticamente.

### Guarda anche

* class [MarkdownSaveOptions](../../markdownsaveoptions)
* spazio dei nomi [Aspose.Words.Saving](../../markdownsaveoptions)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
