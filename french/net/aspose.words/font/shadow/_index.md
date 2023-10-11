---
title: Font.Shadow
second_title: Référence de l'API Aspose.Words pour .NET
description: Font propriété. True si la police est formatée comme ombrée.
type: docs
weight: 330
url: /fr/net/aspose.words/font/shadow/
---
## Font.Shadow property

True si la police est formatée comme ombrée.

```csharp
public bool Shadow { get; set; }
```

### Exemples

Montre comment créer une séquence de texte formatée avec une ombre.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Définit le drapeau Ombre pour appliquer un effet d'ombre décalé,
// donnant l'impression que les lettres flottent au-dessus de la page.
builder.Font.Shadow = true;
builder.Font.Size = 36;

builder.Writeln("This text has a shadow.");

doc.Save(ArtifactsDir + "Font.Shadow.docx");
```

### Voir également

* class [Font](../)
* espace de noms [Aspose.Words](../../font/)
* Assemblée [Aspose.Words](../../../)


