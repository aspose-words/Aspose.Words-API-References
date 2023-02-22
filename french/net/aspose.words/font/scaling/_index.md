---
title: Font.Scaling
second_title: Référence de l'API Aspose.Words pour .NET
description: Font propriété. Obtient ou définit la mise à léchelle de la largeur des caractères en pourcentage.
type: docs
weight: 310
url: /fr/net/aspose.words/font/scaling/
---
## Font.Scaling property

Obtient ou définit la mise à l'échelle de la largeur des caractères en pourcentage.

```csharp
public int Scaling { get; set; }
```

### Exemples

Montre comment définir la mise à l'échelle horizontale et l'espacement des caractères.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ajoute une suite de texte et augmente la largeur des caractères à 150 %.
builder.Font.Scaling = 150;
builder.Writeln("Wide characters");

// Ajoute une suite de texte et ajoute 1 pt d'espacement horizontal supplémentaire entre chaque caractère.
builder.Font.Spacing = 1;
builder.Writeln("Expanded by 1pt");

// Ajoute une suite de texte et rapproche les caractères de 1 pt.
builder.Font.Spacing = -1;
builder.Writeln("Condensed by 1pt");

doc.Save(ArtifactsDir + "Font.ScalingSpacing.docx");
```

### Voir également

* class [Font](../)
* espace de noms [Aspose.Words](../../font/)
* Assemblée [Aspose.Words](../../../)


