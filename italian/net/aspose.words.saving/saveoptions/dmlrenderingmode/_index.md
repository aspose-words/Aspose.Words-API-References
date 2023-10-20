---
title: SaveOptions.DmlRenderingMode
linktitle: DmlRenderingMode
articleTitle: DmlRenderingMode
second_title: Aspose.Words per .NET
description: SaveOptions DmlRenderingMode proprietà. Ottiene o imposta un valore che determina la modalità di rendering delle forme DrawingML in C#.
type: docs
weight: 70
url: /it/net/aspose.words.saving/saveoptions/dmlrenderingmode/
---
## SaveOptions.DmlRenderingMode property

Ottiene o imposta un valore che determina la modalità di rendering delle forme DrawingML.

```csharp
public DmlRenderingMode DmlRenderingMode { get; set; }
```

## Osservazioni

Il valore predefinito èFallback .

Questa proprietà viene utilizzata quando il documento viene esportato in formati di pagina fissi.

## Esempi

Mostra come eseguire il rendering delle forme di fallback durante il salvataggio in PDF.

```csharp
Document doc = new Document(MyDir + "DrawingML shape fallbacks.docx");

// Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui il metodo converte il documento in .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Imposta la proprietà "DmlRenderingMode" su "DmlRenderingMode.Fallback"
// per sostituire le forme DML con le relative forme di fallback.
// Imposta la proprietà "DmlRenderingMode" su "DmlRenderingMode.DrawingML"
// per eseguire il rendering delle forme DML stesse.
options.DmlRenderingMode = dmlRenderingMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.DrawingMLFallback.pdf", options);
```

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

* enum [DmlRenderingMode](../../dmlrenderingmode/)
* class [SaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
