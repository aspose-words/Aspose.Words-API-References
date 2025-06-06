---
title: HyphenationOptions.ConsecutiveHyphenLimit
linktitle: ConsecutiveHyphenLimit
articleTitle: ConsecutiveHyphenLimit
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ConsecutiveHyphenLimit dans HyphenationOptions. Contrôlez l'utilisation des traits d'union dans votre texte pour une meilleure lisibilité et une meilleure mise en forme. Valeur par défaut  0.
type: docs
weight: 30
url: /fr/net/aspose.words.settings/hyphenationoptions/consecutivehyphenlimit/
---
## HyphenationOptions.ConsecutiveHyphenLimit property

Obtient ou définit le nombre maximal de lignes consécutives pouvant se terminer par des tirets. La valeur par défaut de cette propriété est 0.

```csharp
public int ConsecutiveHyphenLimit { get; set; }
```

## Remarques

Si la valeur de cette propriété est définie sur 0, n'importe quel nombre de lignes consécutives peut se terminer par des tirets.

La propriété n'a pas d'effet lors de l'enregistrement dans des formats de page fixes, par exemple PDF.

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
