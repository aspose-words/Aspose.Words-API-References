---
title: MetafileRenderingOptions.EmfPlusDualRenderingMode
second_title: Aspose.Words per .NET API Reference
description: MetafileRenderingOptions proprietà. Ottiene o imposta un valore che determina la modalità di rendering dei metafile EMF Dual.
type: docs
weight: 20
url: /it/net/aspose.words.saving/metafilerenderingoptions/emfplusdualrenderingmode/
---
## MetafileRenderingOptions.EmfPlusDualRenderingMode property

Ottiene o imposta un valore che determina la modalità di rendering dei metafile EMF+ Dual.

```csharp
public EmfPlusDualRenderingMode EmfPlusDualRenderingMode { get; set; }
```

### Osservazioni

metafile EMF+ Dual contengono parti EMF+ e EMF. MS Word e GDI+ rendono sempre la parte EMF+. Aspose.Words attualmente non supporta completamente tutti i record EMF+ e in alcuni casi il risultato del rendering della parte EMF sembra migliore rispetto al risultato del rendering della parte EMF+.

Questa opzione viene utilizzata solo quando il metafile viene visualizzato come grafica vettoriale. Quando il metafile viene renderizzato in bitmap, viene sempre utilizzata la parte EMF+.

Il valore predefinito èEmfPlusWithFallback.

### Esempi

Mostra come configurare le opzioni di rendering avanzate relative ai metafile di Windows durante il salvataggio in PDF.

```csharp
Document doc = new Document(MyDir + "EMF.docx");

// Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Imposta la proprietà "EmfPlusDualRenderingMode" su "EmfPlusDualRenderingMode.Emf"
// per eseguire il rendering solo della parte EMF di un metafile dual EMF+.
// Imposta la proprietà "EmfPlusDualRenderingMode" su "EmfPlusDualRenderingMode.EmfPlus" su
// per eseguire il rendering della parte EMF+ di un metafile dual EMF+.
// Imposta la proprietà "EmfPlusDualRenderingMode" su "EmfPlusDualRenderingMode.EmfPlusWithFallback"
// per eseguire il rendering della parte EMF+ di un doppio metafile EMF+ se tutti i record EMF+ sono supportati.
// Altrimenti, Aspose.Words renderà la parte EMF.
saveOptions.MetafileRenderingOptions.EmfPlusDualRenderingMode = renderingMode;

// Imposta la proprietà "UseEmfEmbeddedToWmf" su "true" per eseguire il rendering dei dati EMF incorporati
// per i metafile che possiamo renderizzare come grafica vettoriale.
saveOptions.MetafileRenderingOptions.UseEmfEmbeddedToWmf = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.RenderMetafile.pdf", saveOptions);
```

### Guarda anche

* enum [EmfPlusDualRenderingMode](../../emfplusdualrenderingmode/)
* class [MetafileRenderingOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../metafilerenderingoptions/)
* assemblea [Aspose.Words](../../../)


