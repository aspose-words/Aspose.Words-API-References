---
title: SaveOptions.ImlRenderingMode
linktitle: ImlRenderingMode
articleTitle: ImlRenderingMode
second_title: Aspose.Words per .NET
description: Scopri come la proprietà SaveOptions ImlRenderingMode migliora il rendering degli oggetti InkML. Ottimizza il rendering dell'inchiostro per risultati visivi migliori!
type: docs
weight: 90
url: /it/net/aspose.words.saving/saveoptions/imlrenderingmode/
---
## SaveOptions.ImlRenderingMode property

Ottiene o imposta un valore che determina come vengono renderizzati gli oggetti ink (InkML).

```csharp
public ImlRenderingMode ImlRenderingMode { get; set; }
```

## Osservazioni

Il valore predefinito èInkML .

Questa proprietà viene utilizzata quando il documento viene esportato in formati di pagina fissi.

## Esempi

Mostra come eseguire il rendering dell'oggetto Ink.

```csharp
Document doc = new Document(MyDir + "Ink object.docx");

// L'impostazione 'ImlRenderingMode.InkML' ignora la forma di fallback dell'oggetto ink (InkML) ed esegue il rendering di InkML stesso.
// Se il risultato del rendering non è soddisfacente,
// utilizzare 'ImlRenderingMode.Fallback' per ottenere un risultato simile alle versioni precedenti.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Jpeg)
{
    ImlRenderingMode = ImlRenderingMode.InkML
};

doc.Save(ArtifactsDir + "ImageSaveOptions.RenderInkObject.jpeg", saveOptions);
```

### Guarda anche

* enum [ImlRenderingMode](../../imlrenderingmode/)
* class [SaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
