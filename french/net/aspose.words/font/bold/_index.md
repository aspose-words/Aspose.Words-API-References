---
title: Font.Bold
second_title: Référence de l'API Aspose.Words pour .NET
description: Font propriété. Vrai si la police est formatée en gras.
type: docs
weight: 40
url: /fr/net/aspose.words/font/bold/
---
## Font.Bold property

Vrai si la police est formatée en gras.

```csharp
public bool Bold { get; set; }
```

### Exemples

Montre comment insérer du texte formaté à l'aide de DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Spécifiez la mise en forme de la police, puis ajoutez du texte.
Aspose.Words.Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Courier New";
font.Underline = Underline.Dash;

builder.Write("Hello world!");
```

### Voir également

* class [Font](../)
* espace de noms [Aspose.Words](../../font/)
* Assemblée [Aspose.Words](../../../)


