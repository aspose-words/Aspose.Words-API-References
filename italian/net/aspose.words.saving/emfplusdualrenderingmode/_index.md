---
title: EmfPlusDualRenderingMode Enum
linktitle: EmfPlusDualRenderingMode
articleTitle: EmfPlusDualRenderingMode
second_title: Aspose.Words per .NET
description: Scopri l'enum EMF Plus Dual Rendering Mode di Aspose.Words per un rendering ottimale dei metafile EMF Dual. Migliora l'elaborazione dei tuoi documenti con precisione!
type: docs
weight: 5730
url: /it/net/aspose.words.saving/emfplusdualrenderingmode/
---
## EmfPlusDualRenderingMode enumeration

Specifica come Aspose.Words dovrebbe eseguire il rendering dei metafile EMF+ Dual.

```csharp
public enum EmfPlusDualRenderingMode
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| EmfPlusWithFallback | `0` | Aspose.Words tenta di eseguire il rendering di parte EMF+ del metafile EMF+ Dual. Se alcuni record EMF+ non sono supportati , Aspose.Words esegue il rendering di parte EMF del metafile EMF+ Dual. |
| EmfPlus | `1` | Aspose.Words esegue il rendering di EMF+ come parte del metafile EMF+ Dual. |
| Emf | `2` | Aspose.Words esegue il rendering di EMF come parte del metafile EMF+ Dual. |

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

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
