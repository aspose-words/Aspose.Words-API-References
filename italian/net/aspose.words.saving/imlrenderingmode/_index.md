---
title: ImlRenderingMode Enum
linktitle: ImlRenderingMode
articleTitle: ImlRenderingMode
second_title: Aspose.Words per .NET
description: Aspose.Words.Saving.ImlRenderingMode enum. Specifica la modalità di rendering degli oggetti input penna InkML nei formati di pagina fissi in C#.
type: docs
weight: 5250
url: /it/net/aspose.words.saving/imlrenderingmode/
---
## ImlRenderingMode enumeration

Specifica la modalità di rendering degli oggetti input penna (InkML) nei formati di pagina fissi.

```csharp
public enum ImlRenderingMode
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Fallback | `0` | Se la forma di fallback è disponibile per l'oggetto ink (InkML), Aspose.Words esegue il rendering della forma di fallback invece di InkML. |
| InkML | `1` | Aspose.Words ignora la forma di riserva dell'oggetto Ink (InkML) ed esegue il rendering di InkML stesso. Questa è la modalità predefinita. |

## Esempi

Mostra come eseguire il rendering dell'oggetto Ink.

```csharp
Document doc = new Document(MyDir + "Ink object.docx");

// Imposta 'ImlRenderingMode.InkML' ignora la forma fallback dell'oggetto Ink (InkML) ed esegue il rendering di InkML stesso.
// Se il risultato del rendering non è soddisfacente,
// utilizzare 'ImlRenderingMode.Fallback' per ottenere un risultato simile alle versioni precedenti.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Jpeg)
{
    ImlRenderingMode = ImlRenderingMode.InkML
};

doc.Save(ArtifactsDir + "ImageSaveOptions.RenderInkObject.jpeg", saveOptions);
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
