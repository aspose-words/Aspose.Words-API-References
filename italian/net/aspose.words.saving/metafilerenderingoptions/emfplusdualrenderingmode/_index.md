---
title: MetafileRenderingOptions.EmfPlusDualRenderingMode
linktitle: EmfPlusDualRenderingMode
articleTitle: EmfPlusDualRenderingMode
second_title: Aspose.Words per .NET
description: Scopri come la proprietà EmfPlusDualRenderingMode migliora il rendering dei metafile EMF Dual. Ottimizza la tua grafica con opzioni di rendering flessibili oggi stesso!
type: docs
weight: 20
url: /it/net/aspose.words.saving/metafilerenderingoptions/emfplusdualrenderingmode/
---
## MetafileRenderingOptions.EmfPlusDualRenderingMode property

Ottiene o imposta un valore che determina come devono essere renderizzati i metafile EMF+ Dual.

```csharp
public EmfPlusDualRenderingMode EmfPlusDualRenderingMode { get; set; }
```

## Osservazioni

I metafile EMF+ Dual contengono sia parti EMF+ che EMF. MS Word e GDI+ eseguono sempre il rendering della parte EMF+. Aspose.Words attualmente non supporta completamente tutti i record EMF+ e in alcuni casi il rendering del risultato della parte EMF ha un aspetto migliore rispetto al rendering del risultato della parte EMF+.

Questa opzione viene utilizzata solo quando il metafile viene renderizzato come grafica vettoriale. Quando il metafile viene renderizzato in bitmap, la parte EMF+ viene sempre utilizzata.

Il valore predefinito èEmfPlusWithFallback.

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

* enum [EmfPlusDualRenderingMode](../../emfplusdualrenderingmode/)
* class [MetafileRenderingOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
