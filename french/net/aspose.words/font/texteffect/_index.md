---
title: Font.TextEffect
linktitle: TextEffect
articleTitle: TextEffect
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Font TextEffect pour personnaliser facilement les animations de polices, en améliorant vos conceptions avec des effets de texte dynamiques pour une expérience utilisateur captivante.
type: docs
weight: 460
url: /fr/net/aspose.words/font/texteffect/
---
## Font.TextEffect property

Obtient ou définit l'effet d'animation de la police.

```csharp
public TextEffect TextEffect { get; set; }
```

## Exemples

Montre comment appliquer un effet visuel à une course.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 36;
builder.Font.TextEffect = TextEffect.SparkleText;

builder.Writeln("Text with a sparkle effect.");

// Les anciennes versions de Microsoft Word ne prennent en charge que les effets d’animation de police.
doc.Save(ArtifactsDir + "Font.SparklingText.doc");
```

### Voir également

* enum [TextEffect](../../texteffect/)
* class [Font](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
