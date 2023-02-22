---
title: Enum ImlRenderingMode
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Saving.ImlRenderingMode enum. Specifica la modalità di rendering degli oggetti Ink InkML in formati di pagina fissi.
type: docs
weight: 4990
url: /it/net/aspose.words.saving/imlrenderingmode/
---
## ImlRenderingMode enumeration

Specifica la modalità di rendering degli oggetti Ink (InkML) in formati di pagina fissi.

```csharp
public enum ImlRenderingMode
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Fallback | `0` | Se la forma di fallback è disponibile per l'oggetto Ink (InkML), Aspose.Words esegue il rendering della forma di fallback invece di InkML. |
| InkML | `1` | Aspose.Words ignora l'oggetto della forma di fallback dell'inchiostro (InkML) ed esegue il rendering di InkML stesso. Questa è la modalità predefinita. |

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

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)


