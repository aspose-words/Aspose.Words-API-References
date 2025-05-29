---
title: ImageColorMode Enum
linktitle: ImageColorMode
articleTitle: ImageColorMode
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Saving.ImageColorMode per ottimizzare le immagini delle pagine dei documenti. Controlla le modalità colore per una migliore qualità visiva nei tuoi progetti.
type: docs
weight: 5960
url: /it/net/aspose.words.saving/imagecolormode/
---
## ImageColorMode enumeration

Specifica la modalità colore per le immagini generate delle pagine del documento.

```csharp
public enum ImageColorMode
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | `0` | Le pagine del documento verranno visualizzate come immagini a colori. |
| Grayscale | `1` | Le pagine del documento verranno visualizzate come immagini in scala di grigi. |
| BlackAndWhite | `2` | Le pagine del documento verranno visualizzate come immagini in bianco e nero. |

## Esempi

Mostra come impostare una modalità colore durante il rendering dei documenti.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Quando salviamo il documento come immagine, possiamo passare un oggetto SaveOptions a
// seleziona una modalità colore per l'immagine che verrà generata dall'operazione di salvataggio.
// Se impostiamo la proprietà "ImageColorMode" su "ImageColorMode.BlackAndWhite",
// l'operazione di salvataggio applicherà una riduzione del colore in scala di grigi durante il rendering del documento.
 // Se impostiamo la proprietà "ImageColorMode" su "ImageColorMode.Grayscale",
// l'operazione di salvataggio trasformerà il documento in un'immagine monocromatica.
// Se impostiamo la proprietà "ImageColorMode" su "None", l'operazione di salvataggio applicherà il metodo predefinito
// e conserva tutti i colori del documento nell'immagine di output.
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.ImageColorMode = imageColorMode;

doc.Save(ArtifactsDir + "ImageSaveOptions.ColorMode.png", imageSaveOptions);
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
