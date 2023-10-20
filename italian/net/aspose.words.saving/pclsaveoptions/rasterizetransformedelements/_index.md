---
title: PclSaveOptions.RasterizeTransformedElements
linktitle: RasterizeTransformedElements
articleTitle: RasterizeTransformedElements
second_title: Aspose.Words per .NET
description: PclSaveOptions RasterizeTransformedElements proprietà. Ottiene o imposta un valore che determina se gli elementi trasformati complessi devono essere rasterizzati o meno prima di essere salvati nel documento PCL. Limpostazione predefinita èVERO  in C#.
type: docs
weight: 30
url: /it/net/aspose.words.saving/pclsaveoptions/rasterizetransformedelements/
---
## PclSaveOptions.RasterizeTransformedElements property

Ottiene o imposta un valore che determina se gli elementi trasformati complessi devono essere rasterizzati o meno prima di essere salvati nel documento PCL. L'impostazione predefinita è`VERO` .

```csharp
public bool RasterizeTransformedElements { get; set; }
```

## Osservazioni

PCL non supporta alcuni tipi di trasformazioni utilizzate da Aspose Words. Ad esempio immagini ruotate e inclinate e pennelli texture. Per visualizzare correttamente tali elementi viene utilizzato il processo di rasterizzazione, ovvero il salvataggio nell'immagine e il ritaglio. Questo processo può richiedere tempo e memoria aggiuntivi. Se il flag è impostato su`falso` , alcuni contenuti nell'output potrebbero essere diversi rispetto al documento di origine.

## Esempi

Mostra come rasterizzare elementi complessi durante il salvataggio di un documento su PCL.

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
