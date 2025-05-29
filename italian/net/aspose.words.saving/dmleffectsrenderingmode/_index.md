---
title: DmlEffectsRenderingMode Enum
linktitle: DmlEffectsRenderingMode
articleTitle: DmlEffectsRenderingMode
second_title: Aspose.Words per .NET
description: Scopri l'enum DmlEffectsRenderingMode di Aspose.Words per un rendering ottimizzato degli effetti DrawingML nei formati di pagina fissi. Migliora la qualità dei tuoi documenti!
type: docs
weight: 5660
url: /it/net/aspose.words.saving/dmleffectsrenderingmode/
---
## DmlEffectsRenderingMode enumeration

Specifica come gli effetti DrawingML vengono renderizzati nei formati di pagina fissi.

```csharp
public enum DmlEffectsRenderingMode
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Simplified | `0` | Il rendering degli effetti DrawingML è semplificato. |
| None | `1` | Non vengono renderizzati effetti DrawingML. |
| Fine | `2` | Gli effetti DrawingML vengono renderizzati in modalità fine che implica un'elaborazione avanzata. In questa modalità il rendering degli effetti fornisce risultati migliori ma a un costo di prestazioni più elevato rispetto aSimplified modalità. |

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

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
