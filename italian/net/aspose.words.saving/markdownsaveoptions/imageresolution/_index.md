---
title: MarkdownSaveOptions.ImageResolution
linktitle: ImageResolution
articleTitle: ImageResolution
second_title: Aspose.Words per .NET
description: Ottimizza le tue esportazioni Markdown con la proprietà ImageResolution, impostando risoluzioni di output personalizzate per immagini più nitide. Predefinito: 96 dpi.
type: docs
weight: 60
url: /it/net/aspose.words.saving/markdownsaveoptions/imageresolution/
---
## MarkdownSaveOptions.ImageResolution property

Specifica la risoluzione di output per le immagini durante l'esportazione in Markdown. Il valore predefinito è`96 dpi` .

```csharp
public int ImageResolution { get; set; }
```

## Esempi

Mostra come impostare la risoluzione di output per le immagini.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.ImageResolution = 300;

doc.Save(ArtifactsDir + "MarkdownSaveOptions.ImageResolution.md", saveOptions);
```

### Guarda anche

* class [MarkdownSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
