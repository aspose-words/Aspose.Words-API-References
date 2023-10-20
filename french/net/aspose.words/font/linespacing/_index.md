---
title: Font.LineSpacing
linktitle: LineSpacing
articleTitle: LineSpacing
second_title: Aspose.Words pour .NET
description: Font LineSpacing propriété. Renvoie lespacement des lignes de cette police en points en C#.
type: docs
weight: 190
url: /fr/net/aspose.words/font/linespacing/
---
## Font.LineSpacing property

Renvoie l'espacement des lignes de cette police (en points).

```csharp
public double LineSpacing { get; }
```

## Exemples

Montre comment obtenir l’interligne d’une police, en points.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Définissez différentes polices pour DocumentBuilder et vérifiez leur espacement des lignes.
builder.Font.Name = "Calibri";
Assert.AreEqual(14.6484375d, builder.Font.LineSpacing);

builder.Font.Name = "Times New Roman";
Assert.AreEqual(13.798828125d, builder.Font.LineSpacing);
```

### Voir également

* class [Font](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
