---
title: SvgSaveOptions.TextOutputMode
linktitle: TextOutputMode
articleTitle: TextOutputMode
second_title: Aspose.Words per .NET
description: SvgSaveOptions TextOutputMode proprietà. Ottiene o imposta un valore che determina come deve essere visualizzato il testo in SVG in C#.
type: docs
weight: 90
url: /it/net/aspose.words.saving/svgsaveoptions/textoutputmode/
---
## SvgSaveOptions.TextOutputMode property

Ottiene o imposta un valore che determina come deve essere visualizzato il testo in SVG.

```csharp
public SvgTextOutputMode TextOutputMode { get; set; }
```

## Osservazioni

Utilizza questa proprietà per ottenere o impostare la modalità di rendering del testo all'interno di un documento durante il salvataggio in formato SVG.

Il valore predefinito èUseTargetMachineFonts.

## Esempi

Mostra come imitare le proprietà delle immagini durante la conversione di un documento .docx in .svg.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// Configura l'oggetto SvgSaveOptions per il salvataggio senza bordi della pagina o testo selezionabile.
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
