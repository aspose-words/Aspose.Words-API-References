---
title: Font.Spacing
second_title: Référence de l'API Aspose.Words pour .NET
description: Font propriété. Renvoie ou définit lespacement en points entre les caractères .
type: docs
weight: 380
url: /fr/net/aspose.words/font/spacing/
---
## Font.Spacing property

Renvoie ou définit l'espacement (en points) entre les caractères .

```csharp
public double Spacing { get; set; }
```

### Exemples

Montre comment définir la mise à l’échelle et l’espacement horizontaux des caractères.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ajoutez une séquence de texte et augmentez la largeur des caractères à 150 %.
builder.Font.Scaling = 150;
builder.Writeln("Wide characters");

// Ajoutez une séquence de texte et ajoutez 1 pt d'espacement horizontal supplémentaire entre chaque caractère.
builder.Font.Spacing = 1;
builder.Writeln("Expanded by 1pt");

// Ajoutez une séquence de texte et rapprochez les caractères de 1 pt.
builder.Font.Spacing = -1;
builder.Writeln("Condensed by 1pt");

doc.Save(ArtifactsDir + "Font.ScalingSpacing.docx");
```

### Voir également

* class [Font](../)
* espace de noms [Aspose.Words](../../font/)
* Assemblée [Aspose.Words](../../../)


