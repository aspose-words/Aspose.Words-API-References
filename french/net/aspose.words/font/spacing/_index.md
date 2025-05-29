---
title: Font.Spacing
linktitle: Spacing
articleTitle: Spacing
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Espacement des polices pour ajuster facilement l'espacement des caractères en points. Améliorez la lisibilité et la conception grâce à un contrôle typographique précis.
type: docs
weight: 390
url: /fr/net/aspose.words/font/spacing/
---
## Font.Spacing property

Renvoie ou définit l'espacement (en points) entre les caractères .

```csharp
public double Spacing { get; set; }
```

## Exemples

Montre comment définir la mise à l'échelle horizontale et l'espacement des caractères.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ajoutez une série de texte et augmentez la largeur des caractères à 150 %.
builder.Font.Scaling = 150;
builder.Writeln("Wide characters");

// Ajoutez une série de texte et ajoutez 1 pt d'espacement horizontal supplémentaire entre chaque caractère.
builder.Font.Spacing = 1;
builder.Writeln("Expanded by 1pt");

// Ajoutez une série de texte et rapprochez les caractères de 1 pt.
builder.Font.Spacing = -1;
builder.Writeln("Condensed by 1pt");

doc.Save(ArtifactsDir + "Font.ScalingSpacing.docx");
```

### Voir également

* class [Font](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
