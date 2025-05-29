---
title: SvgSaveOptions.FitToViewPort
linktitle: FitToViewPort
articleTitle: FitToViewPort
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété SvgSaveOptions FitToViewPort optimise votre sortie SVG pour remplir parfaitement n'importe quelle fenêtre de navigateur ou conteneur pour des visuels époustouflants.
type: docs
weight: 30
url: /fr/net/aspose.words.saving/svgsaveoptions/fittoviewport/
---
## SvgSaveOptions.FitToViewPort property

Spécifie si le SVG de sortie doit remplir la zone d'affichage disponible (fenêtre de navigateur ou conteneur). Lorsqu'il est défini sur`vrai`la largeur et la hauteur du SVG de sortie sont définies sur 100 %.

La valeur par défaut est`FAUX`.

```csharp
public bool FitToViewPort { get; set; }
```

## Exemples

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
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
