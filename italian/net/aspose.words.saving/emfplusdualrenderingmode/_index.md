---
title: EmfPlusDualRenderingMode Enum
linktitle: EmfPlusDualRenderingMode
articleTitle: EmfPlusDualRenderingMode
second_title: Aspose.Words per .NET
description: Aspose.Words.Saving.EmfPlusDualRenderingMode enum. Specifica come Aspose.Words dovrebbe eseguire il rendering dei metafile EMF Dual in C#.
type: docs
weight: 4980
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
| EmfPlusWithFallback | `0` | Aspose.Words tenta di rendere EMF+ parte del metafile EMF+ Dual. Se alcuni dei record EMF+ non sono supportati , Aspose.Words rende EMF parte di EMF+ Dual metafile. |
| EmfPlus | `1` | Aspose.Words rende EMF+ parte di EMF+ Dual metafile. |
| Emf | `2` | Aspose.Words rende EMF parte di EMF+ Dual metafile. |

## Esempi

Mostra come configurare le opzioni di rendering relative a Enhanced Windows Metafile durante il salvataggio in PDF.

```csharp
Document doc = new Document(MyDir + "EMF.docx");

// Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui il metodo converte il documento in .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Imposta la proprietà "EmfPlusDualRenderingMode" su "EmfPlusDualRenderingMode.Emf"
// per eseguire il rendering solo della parte EMF di un doppio metafile EMF+.
// Imposta la proprietà "EmfPlusDualRenderingMode" su "EmfPlusDualRenderingMode.EmfPlus" su
// per eseguire il rendering della parte EMF+ di un doppio metafile EMF+.
// Imposta la proprietà "EmfPlusDualRenderingMode" su "EmfPlusDualRenderingMode.EmfPlusWithFallback"
// per eseguire il rendering della parte EMF+ di un doppio metafile EMF+ se tutti i record EMF+ sono supportati.
// Altrimenti, Aspose.Words renderà la parte EMF.
saveOptions.MetafileRenderingOptions.EmfPlusDualRenderingMode = renderingMode;

// Imposta la proprietà "UseEmfEmbeddedToWmf" su "true" per eseguire il rendering dei dati EMF incorporati
// per i metafile che possiamo visualizzare come grafica vettoriale.
saveOptions.MetafileRenderingOptions.UseEmfEmbeddedToWmf = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.RenderMetafile.pdf", saveOptions);
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
