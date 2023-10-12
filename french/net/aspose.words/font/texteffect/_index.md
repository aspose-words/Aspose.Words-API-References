---
title: Font.TextEffect
second_title: Référence de l'API Aspose.Words pour .NET
description: Font propriété. Obtient ou définit leffet danimation de la police.
type: docs
weight: 450
url: /fr/net/aspose.words/font/texteffect/
---
## Font.TextEffect property

Obtient ou définit l'effet d'animation de la police.

```csharp
public TextEffect TextEffect { get; set; }
```

### Exemples

Montre comment appliquer un effet visuel à une exécution.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 36;
builder.Font.TextEffect = TextEffect.SparkleText;

builder.Writeln("Text with a sparkle effect.");

// Les anciennes versions de Microsoft Word ne prennent en charge que les effets d'animation de polices.
doc.Save(ArtifactsDir + "Font.SparklingText.doc");
```

### Voir également

* enum [TextEffect](../../texteffect/)
* class [Font](../)
* espace de noms [Aspose.Words](../../font/)
* Assemblée [Aspose.Words](../../../)


