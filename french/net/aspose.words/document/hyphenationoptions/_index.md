---
title: Document.HyphenationOptions
linktitle: HyphenationOptions
articleTitle: HyphenationOptions
second_title: Aspose.Words pour .NET
description: Explorez la propriété Document HyphenationOptions pour personnaliser les paramètres de césure, améliorant ainsi la lisibilité et la présentation de votre document.
type: docs
weight: 220
url: /fr/net/aspose.words/document/hyphenationoptions/
---
## Document.HyphenationOptions property

Donne accès aux options de césure du document.

```csharp
public HyphenationOptions HyphenationOptions { get; }
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

* class [HyphenationOptions](../../../aspose.words.settings/hyphenationoptions/)
* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
