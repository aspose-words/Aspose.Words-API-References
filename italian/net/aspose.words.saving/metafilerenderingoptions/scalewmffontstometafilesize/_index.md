---
title: MetafileRenderingOptions.ScaleWmfFontsToMetafileSize
second_title: Aspose.Words per .NET API Reference
description: MetafileRenderingOptions proprietà. Ottiene o imposta un valore che determina se ridimensionare o meno i caratteri nel metafile WMF in base alla dimensione del metafile nella pagina.
type: docs
weight: 50
url: /it/net/aspose.words.saving/metafilerenderingoptions/scalewmffontstometafilesize/
---
## MetafileRenderingOptions.ScaleWmfFontsToMetafileSize property

Ottiene o imposta un valore che determina se ridimensionare o meno i caratteri nel metafile WMF in base alla dimensione del metafile nella pagina.

```csharp
public bool ScaleWmfFontsToMetafileSize { get; set; }
```

### Osservazioni

Quando i metafile WMF vengono visualizzati in MS Word, i caratteri possono essere ridimensionati in base alle dimensioni effettive del metafile nella pagina.

Quando questo valore è impostato su`VERO`, Aspose.Words emula il ridimensionamento dei caratteri in base alle dimensioni del metafile nella pagina.

Quando questo valore è impostato su`falso`, Aspose.Words visualizza i caratteri mentre il metafile viene renderizzato alla dimensione predefinita.

Questa opzione viene utilizzata solo quando il metafile viene visualizzato come grafica vettoriale.

Il valore predefinito è`VERO`.

### Esempi

Mostra come ridimensionare i caratteri WMF in base alle dimensioni del metafile nella pagina.

```csharp
Document doc = new Document(MyDir + "WMF with text.docx");

// Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Imposta la proprietà "ScaleWmfFontsToMetafileSize" su "true" per ridimensionare i caratteri
// che formatta il testo all'interno delle immagini WMF in base alla dimensione del metafile nella pagina.
// Imposta la proprietà "ScaleWmfFontsToMetafileSize" su "false" su
// conserva la scala predefinita di questi caratteri.
saveOptions.MetafileRenderingOptions.ScaleWmfFontsToMetafileSize = scaleWmfFonts;

doc.Save(ArtifactsDir + "PdfSaveOptions.FontsScaledToMetafileSize.pdf", saveOptions);
```

### Guarda anche

* class [MetafileRenderingOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../metafilerenderingoptions/)
* assemblea [Aspose.Words](../../../)


