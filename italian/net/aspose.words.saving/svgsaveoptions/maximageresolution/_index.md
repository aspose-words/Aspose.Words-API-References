---
title: SvgSaveOptions.MaxImageResolution
linktitle: MaxImageResolution
articleTitle: MaxImageResolution
second_title: Aspose.Words per .NET
description: Controlla la qualità delle immagini raster esportate con SvgSaveOptions MaxImageResolution. Imposta la densità di pixel per risultati ottimali. Il valore predefinito è 0.
type: docs
weight: 50
url: /it/net/aspose.words.saving/svgsaveoptions/maximageresolution/
---
## SvgSaveOptions.MaxImageResolution property

Ottiene o imposta un valore in pixel per pollice che limita la risoluzione delle immagini raster esportate. Il valore predefinito è zero.

```csharp
public int MaxImageResolution { get; set; }
```

## Osservazioni

Se il valore di questa proprietà è diverso da zero, limita la risoluzione delle immagini raster esportate. Vale a dire, le immagini ad alta risoluzione vengono ricampionate fino al limite e le immagini a bassa risoluzione vengono esportate così come sono.

Se il valore di questa proprietà è zero, tutte le immagini raster vengono esportate senza ricampionamento.

## Esempi

Mostra come impostare un limite per la risoluzione dell'immagine.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

SvgSaveOptions saveOptions = new SvgSaveOptions();
saveOptions.MaxImageResolution = 72;

doc.Save(ArtifactsDir + "SvgSaveOptions.MaxImageResolution.svg", saveOptions);
```

### Guarda anche

* class [SvgSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
