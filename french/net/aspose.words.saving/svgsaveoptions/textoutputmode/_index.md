---
title: SvgSaveOptions.TextOutputMode
linktitle: TextOutputMode
articleTitle: TextOutputMode
second_title: Aspose.Words pour .NET
description: SvgSaveOptions TextOutputMode propriété. Obtient ou définit une valeur déterminant la façon dont le texte doit être rendu dans SVG en C#.
type: docs
weight: 90
url: /fr/net/aspose.words.saving/svgsaveoptions/textoutputmode/
---
## SvgSaveOptions.TextOutputMode property

Obtient ou définit une valeur déterminant la façon dont le texte doit être rendu dans SVG.

```csharp
public SvgTextOutputMode TextOutputMode { get; set; }
```

## Remarques

Utilisez cette propriété pour obtenir ou définir le mode de rendu du texte à l'intérieur d'un document lors de l'enregistrement au format SVG.

La valeur par défaut estUseTargetMachineFonts.

## Exemples

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

* enum [SvgTextOutputMode](../../svgtextoutputmode/)
* class [SvgSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
