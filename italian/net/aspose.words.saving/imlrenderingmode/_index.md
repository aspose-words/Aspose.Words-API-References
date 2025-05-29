---
title: ImlRenderingMode Enum
linktitle: ImlRenderingMode
articleTitle: ImlRenderingMode
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words ImlRenderingMode per un rendering InkML ottimale. Migliora l'output dei tuoi documenti con una visualizzazione precisa degli oggetti inchiostro!
type: docs
weight: 6000
url: /it/net/aspose.words.saving/imlrenderingmode/
---
## ImlRenderingMode enumeration

Specifica come gli oggetti ink (InkML) vengono renderizzati in formati di pagina fissi.

```csharp
public enum ImlRenderingMode
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Fallback | `0` | Se è disponibile una forma di fallback per l'oggetto inchiostro (InkML), Aspose.Words esegue il rendering della forma di fallback anziché di InkML. |
| InkML | `1` | Aspose.Words ignora la forma di fallback dell'oggetto ink (InkML) ed esegue il rendering di InkML stesso. Questa è la modalità predefinita. |

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

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
