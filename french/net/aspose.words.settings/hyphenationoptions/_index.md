---
title: HyphenationOptions Class
linktitle: HyphenationOptions
articleTitle: HyphenationOptions
second_title: Aspose.Words pour .NET
description: Aspose.Words.Settings.HyphenationOptions classe. Permet de configurer les options de césure du document en C#.
type: docs
weight: 5790
url: /fr/net/aspose.words.settings/hyphenationoptions/
---
## HyphenationOptions class

Permet de configurer les options de césure du document.

Pour en savoir plus, visitez le[Travailler avec la césure](https://docs.aspose.com/words/net/working-with-hyphenation/) article documentaire.

```csharp
public class HyphenationOptions
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [HyphenationOptions](hyphenationoptions/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [AutoHyphenation](../../aspose.words.settings/hyphenationoptions/autohyphenation/) { get; set; } | Obtient ou définit la valeur déterminant si la césure automatique est activée pour le document. La valeur par défaut de cette propriété est`FAUX` . |
| [ConsecutiveHyphenLimit](../../aspose.words.settings/hyphenationoptions/consecutivehyphenlimit/) { get; set; } | Obtient ou définit le nombre maximum de lignes consécutives pouvant se terminer par des traits d'union. La valeur par défaut de cette propriété est 0. |
| [HyphenateCaps](../../aspose.words.settings/hyphenationoptions/hyphenatecaps/) { get; set; } | Obtient ou définit la valeur déterminant si les mots écrits en majuscules sont coupés. La valeur par défaut de cette propriété est`vrai` . |
| [HyphenationZone](../../aspose.words.settings/hyphenationoptions/hyphenationzone/) { get; set; } | Obtient ou définit la distance en 1/20 de point à partir de la marge droite à l'intérieur de laquelle vous ne souhaitez pas couper les mots. La valeur par défaut de cette propriété est 360 (0,25 pouce). |

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

* espace de noms [Aspose.Words.Settings](../../aspose.words.settings/)
* Assemblée [Aspose.Words](../../)
