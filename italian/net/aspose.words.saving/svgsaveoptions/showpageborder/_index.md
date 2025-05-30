---
title: SvgSaveOptions.ShowPageBorder
linktitle: ShowPageBorder
articleTitle: ShowPageBorder
second_title: Aspose.Words per .NET
description: Scopri la proprietà ShowPageBorder di SvgSaveOptions per personalizzare il contorno della tua pagina. Controlla i bordi senza sforzo l'impostazione predefinita è "true" per un utilizzo semplice!
type: docs
weight: 110
url: /it/net/aspose.words.saving/svgsaveoptions/showpageborder/
---
## SvgSaveOptions.ShowPageBorder property

Controlla se un bordo viene aggiunto al contorno della pagina. Il valore predefinito è`VERO` .

```csharp
public bool ShowPageBorder { get; set; }
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
