---
title: HyphenationOptions.HyphenateCaps
linktitle: HyphenateCaps
articleTitle: HyphenateCaps
second_title: Aspose.Words pour .NET
description: Découvrez la propriété HyphenateCaps dans HyphenationOptions. Contrôlez facilement la césure des mots en majuscules ; la valeur par défaut est « true ». Optimisez votre texte dès aujourd'hui !
type: docs
weight: 40
url: /fr/net/aspose.words.settings/hyphenationoptions/hyphenatecaps/
---
## HyphenationOptions.HyphenateCaps property

Obtient ou définit une valeur déterminant si les mots écrits en majuscules sont coupés. La valeur par défaut de cette propriété est`vrai` .

```csharp
public bool HyphenateCaps { get; set; }
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
