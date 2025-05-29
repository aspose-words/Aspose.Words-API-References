---
title: SaveOptions.DmlEffectsRenderingMode
linktitle: DmlEffectsRenderingMode
articleTitle: DmlEffectsRenderingMode
second_title: Aspose.Words per .NET
description: Scopri come la proprietà SaveOptions DmlEffectsRenderingMode ottimizza il rendering degli effetti DrawingML per migliorare la qualità e le prestazioni dei documenti.
type: docs
weight: 60
url: /it/net/aspose.words.saving/saveoptions/dmleffectsrenderingmode/
---
## SaveOptions.DmlEffectsRenderingMode property

Ottiene o imposta un valore che determina come vengono renderizzati gli effetti DrawingML.

```csharp
public virtual DmlEffectsRenderingMode DmlEffectsRenderingMode { get; set; }
```

## Osservazioni

Il valore predefinito èSimplified .

Questa proprietà viene utilizzata quando il documento viene esportato in formati di pagina fissi.

## Esempi

Mostra come configurare la qualità di rendering degli effetti DrawingML in un documento quando lo salviamo in PDF.

```csharp
Document doc = new Document(MyDir + "DrawingML shape effects.docx");

// Creiamo un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Impostare la proprietà "DmlEffectsRenderingMode" su "DmlEffectsRenderingMode.None" per ignorare tutti gli effetti DrawingML.
// Imposta la proprietà "DmlEffectsRenderingMode" su "DmlEffectsRenderingMode.Simplified"
// per eseguire il rendering di una versione semplificata degli effetti DrawingML.
// Imposta la proprietà "DmlEffectsRenderingMode" su "DmlEffectsRenderingMode.Fine" per
// eseguire il rendering degli effetti DrawingML con maggiore precisione ma anche con maggiori costi di elaborazione.
options.DmlEffectsRenderingMode = effectsRenderingMode;

Assert.AreEqual(DmlRenderingMode.DrawingML, options.DmlRenderingMode);

doc.Save(ArtifactsDir + "PdfSaveOptions.DrawingMLEffects.pdf", options);
```

### Guarda anche

* enum [DmlEffectsRenderingMode](../../dmleffectsrenderingmode/)
* class [SaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
