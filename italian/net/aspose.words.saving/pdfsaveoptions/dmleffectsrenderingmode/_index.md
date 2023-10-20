---
title: PdfSaveOptions.DmlEffectsRenderingMode
linktitle: DmlEffectsRenderingMode
articleTitle: DmlEffectsRenderingMode
second_title: Aspose.Words per .NET
description: PdfSaveOptions DmlEffectsRenderingMode proprietà. Ottiene o imposta un valore che determina la modalità di rendering degli effetti DrawingML in C#.
type: docs
weight: 90
url: /it/net/aspose.words.saving/pdfsaveoptions/dmleffectsrenderingmode/
---
## PdfSaveOptions.DmlEffectsRenderingMode property

Ottiene o imposta un valore che determina la modalità di rendering degli effetti DrawingML.

```csharp
public override DmlEffectsRenderingMode DmlEffectsRenderingMode { get; set; }
```

## Osservazioni

Il valore predefinito èSimplified .

Questa proprietà viene utilizzata quando il documento viene esportato in formati di pagina fissi.

Se[`Compliance`](../compliance/) è impostato perPdfA1a OPdfA1b La proprietà , restituisce sempreNone.

## Esempi

Mostra come configurare la qualità di rendering degli effetti DrawingML in un documento mentre lo salviamo in PDF.

```csharp
Document doc = new Document(MyDir + "DrawingML shape effects.docx");

// Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui il metodo converte il documento in .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Imposta la proprietà "DmlEffectsRenderingMode" su "DmlEffectsRenderingMode.None" per eliminare tutti gli effetti DrawingML.
// Imposta la proprietà "DmlEffectsRenderingMode" su "DmlEffectsRenderingMode.Simplified"
// per eseguire il rendering di una versione semplificata degli effetti DrawingML.
// Imposta la proprietà "DmlEffectsRenderingMode" su "DmlEffectsRenderingMode.Fine" su
// esegue il rendering degli effetti DrawingML con maggiore precisione e anche con maggiori costi di elaborazione.
options.DmlEffectsRenderingMode = effectsRenderingMode;

Assert.AreEqual(DmlRenderingMode.DrawingML, options.DmlRenderingMode);

doc.Save(ArtifactsDir + "PdfSaveOptions.DrawingMLEffects.pdf", options);
```

### Guarda anche

* enum [DmlEffectsRenderingMode](../../dmleffectsrenderingmode/)
* class [PdfSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
