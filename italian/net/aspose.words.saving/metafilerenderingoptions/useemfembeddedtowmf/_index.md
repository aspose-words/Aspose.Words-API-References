---
title: MetafileRenderingOptions.UseEmfEmbeddedToWmf
linktitle: UseEmfEmbeddedToWmf
articleTitle: UseEmfEmbeddedToWmf
second_title: Aspose.Words per .NET
description: Scopri come la proprietà UseEmfEmbeddedToWmf ottimizza il rendering dei metafile WMF, migliorando le prestazioni e la qualità delle tue applicazioni grafiche.
type: docs
weight: 70
url: /it/net/aspose.words.saving/metafilerenderingoptions/useemfembeddedtowmf/
---
## MetafileRenderingOptions.UseEmfEmbeddedToWmf property

Ottiene o imposta un valore che determina come devono essere renderizzati i metafile WMF con metafile EMF incorporati.

```csharp
public bool UseEmfEmbeddedToWmf { get; set; }
```

## Osservazioni

I metafile WMF potrebbero contenere dati EMF incorporati. MS Word nella maggior parte dei casi utilizza dati EMF incorporati. GDI+ utilizza sempre dati WMF.

Quando questo valore è impostato su`VERO`Aspose.Words utilizza dati EMF incorporati durante il rendering.

Quando questo valore è impostato su`falso`Aspose.Words utilizza dati WMF durante il rendering.

Questa opzione viene utilizzata solo quando il metafile viene renderizzato come grafica vettoriale. Quando il metafile viene renderizzato in bitmap, vengono sempre utilizzati i dati WMF.

Il valore predefinito è`VERO`.

## Esempi

Mostra come configurare le opzioni di rendering relative a Enhanced Windows Metafile durante il salvataggio in PDF.

```csharp
Document doc = new Document(MyDir + "EMF.docx");

// Creiamo un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Imposta la proprietà "EmfPlusDualRenderingMode" su "EmfPlusDualRenderingMode.Emf"
// per eseguire il rendering solo della parte EMF di un metafile doppio EMF+.
// Imposta la proprietà "EmfPlusDualRenderingMode" su "EmfPlusDualRenderingMode.EmfPlus" per
// per eseguire il rendering della parte EMF+ di un metafile duale EMF+.
// Imposta la proprietà "EmfPlusDualRenderingMode" su "EmfPlusDualRenderingMode.EmfPlusWithFallback"
// per eseguire il rendering della parte EMF+ di un metafile duale EMF+ se tutti i record EMF+ sono supportati.
// In caso contrario, Aspose.Words eseguirà il rendering della parte EMF.
saveOptions.MetafileRenderingOptions.EmfPlusDualRenderingMode = renderingMode;

// Imposta la proprietà "UseEmfEmbeddedToWmf" su "true" per eseguire il rendering dei dati EMF incorporati
// per i metafile che possiamo riprodurre come grafica vettoriale.
saveOptions.MetafileRenderingOptions.UseEmfEmbeddedToWmf = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.RenderMetafile.pdf", saveOptions);
```

### Guarda anche

* class [MetafileRenderingOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
