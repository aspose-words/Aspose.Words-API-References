---
title: SvgSaveOptions.ShowPageBorder
second_title: Référence de l'API Aspose.Words pour .NET
description: SvgSaveOptions propriété. Contrôle si une bordure est ajoutée au contour de la page. La valeur par défaut estvrai .
type: docs
weight: 80
url: /fr/net/aspose.words.saving/svgsaveoptions/showpageborder/
---
## SvgSaveOptions.ShowPageBorder property

Contrôle si une bordure est ajoutée au contour de la page. La valeur par défaut est`vrai` .

```csharp
public bool ShowPageBorder { get; set; }
```

### Exemples

Montre comment imiter les propriétés des images lors de la conversion d'un document .docx en .svg.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// Configurez l'objet SvgSaveOptions pour enregistrer sans bordures de page ni texte sélectionnable.
SvgSaveOptions options = new SvgSaveOptions
{
    FitToViewPort = true,
    ShowPageBorder = false,
    TextOutputMode = SvgTextOutputMode.UsePlacedGlyphs
};

doc.Save(ArtifactsDir + "SvgSaveOptions.SaveLikeImage.svg", options);
```

### Voir également

* class [SvgSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../svgsaveoptions/)
* Assemblée [Aspose.Words](../../../)


