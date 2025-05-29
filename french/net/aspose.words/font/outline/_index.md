---
title: Font.Outline
linktitle: Outline
articleTitle: Outline
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Contour de police. Formatez facilement vos polices en contours pour une touche design unique. Sublimez votre typographie grâce à cette fonctionnalité simple !
type: docs
weight: 300
url: /fr/net/aspose.words/font/outline/
---
## Font.Outline property

Vrai si la police est formatée en contour.

```csharp
public bool Outline { get; set; }
```

## Exemples

Montre comment créer une série de texte formatée sous forme de plan.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Définissez l'indicateur Contour pour changer la couleur de remplissage du texte en blanc et
 // laissez un contour fin autour de chaque caractère dans la couleur d'origine du texte.
builder.Font.Outline = true;
builder.Font.Color = Color.Blue;
builder.Font.Size = 36;

builder.Writeln("This text has an outline.");

doc.Save(ArtifactsDir + "Font.Outline.docx");
```

### Voir également

* class [Font](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
