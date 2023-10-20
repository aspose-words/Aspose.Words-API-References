---
title: SvgSaveOptions.FitToViewPort
linktitle: FitToViewPort
articleTitle: FitToViewPort
second_title: Aspose.Words per .NET
description: SvgSaveOptions FitToViewPort proprietà. Specifica se lSVG di output deve riempire larea del viewport disponibile finestra del browser o contenitore. Se impostato suVERO la larghezza e laltezza delloutput SVG sono impostate al 100 in C#.
type: docs
weight: 30
url: /it/net/aspose.words.saving/svgsaveoptions/fittoviewport/
---
## SvgSaveOptions.FitToViewPort property

Specifica se l'SVG di output deve riempire l'area del viewport disponibile (finestra del browser o contenitore). Se impostato su`VERO` la larghezza e l'altezza dell'output SVG sono impostate al 100%.

Il valore predefinito è`falso`.

```csharp
public bool FitToViewPort { get; set; }
```

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

* class [SvgSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
