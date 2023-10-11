---
title: SvgSaveOptions.FitToViewPort
second_title: Référence de l'API Aspose.Words pour .NET
description: SvgSaveOptions propriété. Spécifie si le SVG de sortie doit remplir la zone daffichage disponible fenêtre du navigateur ou conteneur. Lorsquil est défini survrai la largeur et la hauteur du SVG de sortie sont définies sur 100.
type: docs
weight: 30
url: /fr/net/aspose.words.saving/svgsaveoptions/fittoviewport/
---
## SvgSaveOptions.FitToViewPort property

Spécifie si le SVG de sortie doit remplir la zone d'affichage disponible (fenêtre du navigateur ou conteneur). Lorsqu'il est défini sur`vrai` la largeur et la hauteur du SVG de sortie sont définies sur 100%.

La valeur par défaut est`FAUX`.

```csharp
public bool FitToViewPort { get; set; }
```

### Exemples

Montre comment imiter les propriétés des images lors de la conversion d'un document .docx en .svg.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// Configurez l'objet SvgSaveOptions pour qu'il soit enregistré sans bordure de page ni texte sélectionnable.
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


