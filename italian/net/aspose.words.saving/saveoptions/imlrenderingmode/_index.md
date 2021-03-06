---
title: ImlRenderingMode
second_title: Aspose.Words per .NET API Reference
description: Ottiene o imposta un valore che determina la modalità di rendering degli oggetti Ink InkML.
type: docs
weight: 100
url: /it/net/aspose.words.saving/saveoptions/imlrenderingmode/
---
## SaveOptions.ImlRenderingMode property

Ottiene o imposta un valore che determina la modalità di rendering degli oggetti Ink (InkML).

```csharp
public ImlRenderingMode ImlRenderingMode { get; set; }
```

### Osservazioni

Il valore predefinito èInkML .

Questa proprietà viene utilizzata quando il documento viene esportato in formati di pagina fissi.

### Esempi

Mostra come eseguire il rendering di un oggetto Ink.

```csharp
Document doc = new Document(MyDir + "Ink object.docx");

// Imposta 'ImlRenderingMode.InkML' ignora l'oggetto Fallback Shape of Ink (InkML) ed esegue il rendering di InkML stesso.
// Se il risultato del rendering non è soddisfacente,
// usa 'ImlRenderingMode.Fallback' per ottenere un risultato simile alle versioni precedenti.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Jpeg)
{
    ImlRenderingMode = ImlRenderingMode.InkML
};

doc.Save(ArtifactsDir + "ImageSaveOptions.RenderInkObject.jpeg", saveOptions);
```

### Guarda anche

* enum [ImlRenderingMode](../../imlrenderingmode)
* class [SaveOptions](../../saveoptions)
* spazio dei nomi [Aspose.Words.Saving](../../saveoptions)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
