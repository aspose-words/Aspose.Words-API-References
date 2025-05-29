---
title: PclSaveOptions.RasterizeTransformedElements
linktitle: RasterizeTransformedElements
articleTitle: RasterizeTransformedElements
second_title: Aspose.Words per .NET
description: Controlla la rasterizzazione di elementi complessi nei documenti PCL con PclSaveOptions. Gestisci facilmente la qualità delle immagini e le dimensioni dei file per risultati ottimali.
type: docs
weight: 30
url: /it/net/aspose.words.saving/pclsaveoptions/rasterizetransformedelements/
---
## PclSaveOptions.RasterizeTransformedElements property

Ottiene o imposta un valore che determina se gli elementi complessi trasformati devono essere rasterizzati prima di essere salvati nel documento PCL. Il valore predefinito è`VERO` .

```csharp
public bool RasterizeTransformedElements { get; set; }
```

## Osservazioni

PCL non supporta alcuni tipi di trasformazioni utilizzate da Aspose Words. Ad esempio, immagini ruotate, inclinate e pennelli texture. Per il rendering corretto di tali elementi viene utilizzato un processo di rasterizzazione, ovvero il salvataggio dell'immagine e il ritaglio. Questo processo può richiedere tempo e memoria aggiuntivi. Se il flag è impostato su`falso` , alcuni contenuti nell'output potrebbero essere diversi rispetto al documento sorgente.

## Esempi

Mostra come rasterizzare elementi complessi durante il salvataggio di un documento in PCL.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

PclSaveOptions saveOptions = new PclSaveOptions
{
    SaveFormat = SaveFormat.Pcl,
    RasterizeTransformedElements = true
};

doc.Save(ArtifactsDir + "PclSaveOptions.RasterizeElements.pcl", saveOptions);
```

### Guarda anche

* class [PclSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
