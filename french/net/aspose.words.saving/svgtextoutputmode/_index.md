---
title: Enum SvgTextOutputMode
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Saving.SvgTextOutputMode énumération. Permet de spécifier comment le texte à lintérieur dun document doit être rendu lors de lenregistrement au format SVG.
type: docs
weight: 5610
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
| UseSvgFonts | `0` | Les polices SVG sont utilisées pour restituer le texte. Notez que tous les navigateurs ne prennent pas en charge les polices SVG. |
| UseTargetMachineFonts | `1` | Les polices installées sur la machine cible sont utilisées pour restituer le texte. Notez que si certaines polices utilisées dans le document ne sont pas disponibles sur la machine cible, le document peut avoir un aspect différent. |
| UsePlacedGlyphs | `2` | Le texte est rendu à l'aide de courbes. Notez que la sélection de texte ne fonctionnera pas si vous utilisez cette option. |

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

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)


