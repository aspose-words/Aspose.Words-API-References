---
title: DmlRenderingMode Enum
linktitle: DmlRenderingMode
articleTitle: DmlRenderingMode
second_title: Aspose.Words per .NET
description: Scopri come Aspose.Words.Saving.DmlRenderingMode migliora il rendering delle forme DrawingML per formati di pagina fissi di alta qualità. Ottimizza gli elementi visivi dei tuoi documenti!
type: docs
weight: 5670
url: /it/net/aspose.words.saving/dmlrenderingmode/
---
## DmlRenderingMode enumeration

Specifica come le forme DrawingML vengono renderizzate in formati di pagina fissi.

```csharp
public enum DmlRenderingMode
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Fallback | `0` | Se la forma di fallback è disponibile per DrawingML, Aspose.Words esegue il rendering della forma di fallback anziché di DrawingML. |
| DrawingML | `1` | Aspose.Words ignora la forma di fallback di DrawingML ed esegue il rendering di DrawingML stesso. Questa è la modalità predefinita. |

## Esempi

Mostra come eseguire il rendering delle forme di fallback durante il salvataggio in PDF.

```csharp
Document doc = new Document(MyDir + "DrawingML shape fallbacks.docx");

// Creiamo un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Imposta la proprietà "DmlRenderingMode" su "DmlRenderingMode.Fallback"
// per sostituire le forme DML con le relative forme di fallback.
// Imposta la proprietà "DmlRenderingMode" su "DmlRenderingMode.DrawingML"
// per eseguire il rendering delle forme DML stesse.
options.DmlRenderingMode = dmlRenderingMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.DrawingMLFallback.pdf", options);
```

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

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
