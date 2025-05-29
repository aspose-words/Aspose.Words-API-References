---
title: SvgSaveOptions.TextOutputMode
linktitle: TextOutputMode
articleTitle: TextOutputMode
second_title: Aspose.Words per .NET
description: Scopri la proprietà TextOutputMode di SvgSaveOptions, che controlla il rendering del testo in SVG per una migliore qualità visiva e personalizzazione. Ottimizza la tua grafica oggi stesso!
type: docs
weight: 120
url: /it/net/aspose.words.saving/svgsaveoptions/textoutputmode/
---
## SvgSaveOptions.TextOutputMode property

Ottiene o imposta un valore che determina come deve essere visualizzato il testo in SVG.

```csharp
public SvgTextOutputMode TextOutputMode { get; set; }
```

## Osservazioni

Utilizzare questa proprietà per ottenere o impostare la modalità di rendering del testo all'interno di un documento quando si salva in formato SVG.

Il valore predefinito èUseTargetMachineFonts.

## Esempi

Mostra come imitare le proprietà delle immagini durante la conversione di un documento .docx in .svg.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// Configurare l'oggetto SvgSaveOptions per salvare senza bordi di pagina o testo selezionabile.
SvgSaveOptions options = new SvgSaveOptions
{
    FitToViewPort = true,
    ShowPageBorder = false,
    TextOutputMode = SvgTextOutputMode.UsePlacedGlyphs
};

doc.Save(ArtifactsDir + "SvgSaveOptions.SaveLikeImage.svg", options);
```

### Guarda anche

* enum [SvgTextOutputMode](../../svgtextoutputmode/)
* class [SvgSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
