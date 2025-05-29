---
title: Font.Scaling
linktitle: Scaling
articleTitle: Scaling
second_title: Aspose.Words pour .NET
description: Découvrez la propriété de mise à l'échelle des polices pour ajuster la largeur des caractères en pourcentage, améliorant ainsi la lisibilité du texte et la flexibilité de conception de vos projets.
type: docs
weight: 320
url: /fr/net/aspose.words/font/scaling/
---
## Font.Scaling property

Obtient ou définit la mise à l'échelle de la largeur des caractères en pourcentage.

```csharp
public int Scaling { get; set; }
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
