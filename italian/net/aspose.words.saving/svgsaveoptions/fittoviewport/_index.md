---
title: SvgSaveOptions.FitToViewPort
linktitle: FitToViewPort
articleTitle: FitToViewPort
second_title: Aspose.Words per .NET
description: Scopri come la proprietà FitToViewPort di SvgSaveOptions ottimizza l'output SVG per riempire perfettamente qualsiasi finestra o contenitore del browser e ottenere immagini straordinarie.
type: docs
weight: 30
url: /it/net/aspose.words.saving/svgsaveoptions/fittoviewport/
---
## SvgSaveOptions.FitToViewPort property

Specifica se l'SVG di output deve riempire l'area di visualizzazione disponibile (finestra del browser o contenitore). Quando impostato su`VERO`larghezza e altezza dell'SVG di output sono impostate al 100%.

Il valore predefinito è`falso`.

```csharp
public bool FitToViewPort { get; set; }
```

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

* class [SvgSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
