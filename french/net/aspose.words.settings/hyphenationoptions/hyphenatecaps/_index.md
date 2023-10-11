---
title: HyphenationOptions.HyphenateCaps
second_title: Référence de l'API Aspose.Words pour .NET
description: HyphenationOptions propriété. Obtient ou définit la valeur déterminant si les mots écrits en majuscules sont coupés. La valeur par défaut de cette propriété estvrai .
type: docs
weight: 40
url: /fr/net/aspose.words.settings/hyphenationoptions/hyphenatecaps/
---
## HyphenationOptions.HyphenateCaps property

Obtient ou définit la valeur déterminant si les mots écrits en majuscules sont coupés. La valeur par défaut de cette propriété est`vrai` .

```csharp
public bool HyphenateCaps { get; set; }
```

### Exemples

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
* espace de noms [Aspose.Words.Settings](../../hyphenationoptions/)
* Assemblée [Aspose.Words](../../../)


