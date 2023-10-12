---
title: Font.Outline
second_title: Référence de l'API Aspose.Words pour .NET
description: Font propriété. True si la police est formatée en outline.
type: docs
weight: 290
url: /fr/net/aspose.words/font/outline/
---
## Font.Outline property

True si la police est formatée en outline.

```csharp
public bool Outline { get; set; }
```

### Exemples

Montre comment créer une séquence de texte formatée sous forme de plan.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Définit l'indicateur de contour pour changer la couleur de remplissage du texte en blanc et
 // laisse un fin contour autour de chaque caractère dans la couleur d'origine du texte.
builder.Font.Outline = true;
builder.Font.Color = Color.Blue;
builder.Font.Size = 36;

builder.Writeln("This text has an outline.");

doc.Save(ArtifactsDir + "Font.Outline.docx");
```

### Voir également

* class [Font](../)
* espace de noms [Aspose.Words](../../font/)
* Assemblée [Aspose.Words](../../../)


