---
title: Enum EmfPlusDualRenderingMode
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Saving.EmfPlusDualRenderingMode enum. Specifica come Aspose.Words deve eseguire il rendering dei metafile EMF Dual.
type: docs
weight: 4720
url: /it/net/aspose.words.saving/emfplusdualrenderingmode/
---
## EmfPlusDualRenderingMode enumeration

Specifica come Aspose.Words deve eseguire il rendering dei metafile EMF+ Dual.

```csharp
public enum EmfPlusDualRenderingMode
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| EmfPlusWithFallback | `0` | Aspose.Words tenta di eseguire il rendering di EMF+ parte del metafile EMF+ Dual. Se alcuni dei record EMF+ non sono supportati , Aspose.Words rende EMF parte del metafile EMF+ Dual. |
| EmfPlus | `1` | Aspose.Words rende EMF+ parte del metafile EMF+ Dual. |
| Emf | `2` | Aspose.Words rende EMF parte del metafile EMF+ Dual. |

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

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)


