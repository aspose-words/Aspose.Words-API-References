---
title: HyphenationOptions.HyphenationZone
linktitle: HyphenationZone
articleTitle: HyphenationZone
second_title: Aspose.Words pour .NET
description: HyphenationOptions HyphenationZone propriété. Obtient ou définit la distance en 1/20 de point à partir de la marge droite à lintérieur de laquelle vous ne souhaitez pas couper les mots. La valeur par défaut de cette propriété est 360 025 pouce en C#.
type: docs
weight: 50
url: /fr/net/aspose.words.settings/hyphenationoptions/hyphenationzone/
---
## HyphenationOptions.HyphenationZone property

Obtient ou définit la distance en 1/20 de point à partir de la marge droite à l'intérieur de laquelle vous ne souhaitez pas couper les mots. La valeur par défaut de cette propriété est 360 (0,25 pouce).

```csharp
public int HyphenationZone { get; set; }
```

## Exemples

Montre comment configurer la césure automatique.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.HyphenationOptions.AutoHyphenation = true;
doc.HyphenationOptions.ConsecutiveHyphenLimit = 2;
doc.HyphenationOptions.HyphenationZone = 720;
doc.HyphenationOptions.HyphenateCaps = true;

doc.Save(ArtifactsDir + "Document.HyphenationOptions.docx");
```

### Voir également

* class [HyphenationOptions](../)
* espace de noms [Aspose.Words.Settings](../../../aspose.words.settings/)
* Assemblée [Aspose.Words](../../../)
