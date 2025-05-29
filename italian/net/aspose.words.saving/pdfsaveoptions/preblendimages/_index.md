---
title: PdfSaveOptions.PreblendImages
linktitle: PreblendImages
articleTitle: PreblendImages
second_title: Aspose.Words per .NET
description: Scopri la proprietà PreblendImages di PdfSaveOptions. Controlla facilmente la fusione di immagini trasparenti per migliorare la qualità del documento e l'impatto visivo.
type: docs
weight: 270
url: /it/net/aspose.words.saving/pdfsaveoptions/preblendimages/
---
## PdfSaveOptions.PreblendImages property

Ottiene o imposta un valore che determina se premiscelare o meno le immagini trasparenti con il colore di sfondo nero.

```csharp
public bool PreblendImages { get; set; }
```

## Osservazioni

La premiscelazione delle immagini può migliorare l'aspetto visivo del documento PDF in Adobe Reader e rimuovere gli artefatti anti-aliasing.

Per visualizzare correttamente le immagini premiscelate, l'applicazione di visualizzazione PDF deve supportare la voce /Matte nel dizionario delle immagini soft-mask. Inoltre, la premiscelazione delle immagini può ridurre le prestazioni di rendering dei PDF.

Il valore predefinito è`falso`.

## Esempi

Mostra come premiscelare immagini con sfondi trasparenti durante il salvataggio di un documento in formato PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Transparent background logo.png");

// Creiamo un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
PdfSaveOptions options = new PdfSaveOptions();
// Imposta la proprietà "PreblendImages" su "true" per premiscelare le immagini trasparenti
// con uno sfondo, che può ridurre gli artefatti.
// Impostare la proprietà "PreblendImages" su "false" per eseguire il rendering normale delle immagini trasparenti.
options.PreblendImages = preblendImages;

doc.Save(ArtifactsDir + "PdfSaveOptions.PreblendImages.pdf", options);
```

### Guarda anche

* class [PdfSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
