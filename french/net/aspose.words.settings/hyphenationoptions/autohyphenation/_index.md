---
title: HyphenationOptions.AutoHyphenation
linktitle: AutoHyphenation
articleTitle: AutoHyphenation
second_title: Aspose.Words pour .NET
description: Contrôlez la césure automatique avec la propriété HyphenationOptions. Améliorez facilement la lisibilité de votre document en activant ou désactivant cette fonctionnalité.
type: docs
weight: 20
url: /fr/net/aspose.words.settings/hyphenationoptions/autohyphenation/
---
## HyphenationOptions.AutoHyphenation property

Obtient ou définit la valeur déterminant si la césure automatique est activée pour le document. La valeur par défaut de cette propriété est`FAUX` .

```csharp
public bool AutoHyphenation { get; set; }
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
