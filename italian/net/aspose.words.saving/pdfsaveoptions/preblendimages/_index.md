---
title: PdfSaveOptions.PreblendImages
second_title: Aspose.Words per .NET API Reference
description: PdfSaveOptions proprietà. Ottiene o imposta un valore che determina se prefondere o meno le immagini trasparenti con il colore di sfondo nero.
type: docs
weight: 260
url: /it/net/aspose.words.saving/pdfsaveoptions/preblendimages/
---
## PdfSaveOptions.PreblendImages property

Ottiene o imposta un valore che determina se prefondere o meno le immagini trasparenti con il colore di sfondo nero.

```csharp
public bool PreblendImages { get; set; }
```

### Osservazioni

La prefusione delle immagini può migliorare l'aspetto visivo del documento PDF in Adobe Reader e rimuovere gli artefatti anti-aliasing.

Per visualizzare correttamente le immagini pre-miscelate, l'applicazione di visualizzazione PDF deve supportare la voce /Matte nel dizionario immagini soft-mask. Inoltre, la pre-miscelazione delle immagini può ridurre le prestazioni di rendering del PDF.

Il valore predefinito è`falso`.

### Esempi

Mostra come prefondere immagini con sfondi trasparenti durante il salvataggio di un documento in PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image img = Image.FromFile(ImageDir + "Transparent background logo.png");
builder.InsertImage(img);

// Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui il metodo converte il documento in .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Imposta la proprietà "PreblendImages" su "true" per prefondere le immagini trasparenti
// con uno sfondo, che può ridurre gli artefatti.
// Imposta la proprietà "PreblendImages" su "false" per eseguire normalmente il rendering delle immagini trasparenti.
options.PreblendImages = preblendImages;

doc.Save(ArtifactsDir + "PdfSaveOptions.PreblendImages.pdf", options);
```

Mostra come prefondere immagini con sfondi trasparenti (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Image image = Image.Decode(ImageDir + "Transparent background logo.png"))
    builder.InsertImage(image);

// Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui il metodo converte il documento in .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Imposta la proprietà "PreblendImages" su "true" per prefondere le immagini trasparenti
// con uno sfondo, che può ridurre gli artefatti.
// Imposta la proprietà "PreblendImages" su "false" per eseguire normalmente il rendering delle immagini trasparenti.
options.PreblendImages = preblendImages;

doc.Save(ArtifactsDir + "PdfSaveOptions.PreblendImagesNetStandard2.pdf", options);
```

### Guarda anche

* class [PdfSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../pdfsaveoptions/)
* assemblea [Aspose.Words](../../../)


