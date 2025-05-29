---
title: SvgTextOutputMode Enum
linktitle: SvgTextOutputMode
articleTitle: SvgTextOutputMode
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Saving.SvgTextOutputMode pour personnaliser le rendu du texte au format SVG, améliorant ainsi la présentation du document et l'attrait visuel.
type: docs
weight: 6410
url: /fr/net/aspose.words.saving/svgtextoutputmode/
---
## SvgTextOutputMode enumeration

Permet de spécifier comment le texte à l'intérieur d'un document doit être rendu lors de l'enregistrement au format SVG.

```csharp
public enum SvgTextOutputMode
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| UseSvgFonts | `0` | Les polices SVG sont utilisées pour afficher du texte. Attention, tous les navigateurs ne prennent pas en charge les polices SVG. |
| UseTargetMachineFonts | `1` | Les polices installées sur la machine cible sont utilisées pour restituer le texte. Notez que si certaines des polices utilisées dans le document ne sont pas disponibles sur la machine cible, le document peut avoir un aspect différent. |
| UsePlacedGlyphs | `2` | Le texte est rendu à l'aide de courbes. Attention, la sélection de texte ne fonctionnera pas avec cette option. |

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

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
