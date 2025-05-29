---
title: Font.Shadow
linktitle: Shadow
articleTitle: Shadow
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Font Shadow, améliorez votre texte avec des effets d'ombre élégants pour un attrait visuel saisissant dans vos créations.
type: docs
weight: 340
url: /fr/net/aspose.words/font/shadow/
---
## Font.Shadow property

Vrai si la police est formatée comme ombrée.

```csharp
public bool Shadow { get; set; }
```

## Exemples

Montre comment créer une série de texte formatée avec une ombre.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Définissez l'indicateur Shadow pour appliquer un effet d'ombre décalé,
// donnant l'impression que les lettres flottent au-dessus de la page.
builder.Font.Shadow = true;
builder.Font.Size = 36;

builder.Writeln("This text has a shadow.");

doc.Save(ArtifactsDir + "Font.Shadow.docx");
```

### Voir également

* class [Font](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
