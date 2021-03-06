---
title: ShowPageBorder
second_title: Aspose.Words per .NET API Reference
description: Controlla se viene aggiunto un bordo al contorno della pagina. Limpostazione predefinita èVERO .
type: docs
weight: 80
url: /it/net/aspose.words.saving/svgsaveoptions/showpageborder/
---
## SvgSaveOptions.ShowPageBorder property

Controlla se viene aggiunto un bordo al contorno della pagina. L'impostazione predefinita è`VERO` .

```csharp
public bool ShowPageBorder { get; set; }
```

### Esempi

Mostra come imitare le proprietà delle immagini durante la conversione di un documento .docx in .svg.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// Configura l'oggetto SvgSaveOptions per il salvataggio senza bordi di pagina o testo selezionabile.
SvgSaveOptions options = new SvgSaveOptions
{
    FitToViewPort = true,
    ShowPageBorder = false,
    TextOutputMode = SvgTextOutputMode.UsePlacedGlyphs
};

doc.Save(ArtifactsDir + "SvgSaveOptions.SaveLikeImage.svg", options);
```

### Guarda anche

* class [SvgSaveOptions](../../svgsaveoptions)
* spazio dei nomi [Aspose.Words.Saving](../../svgsaveoptions)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
