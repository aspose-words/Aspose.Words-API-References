---
title: SplitOptions.SplitCriteria
linktitle: SplitCriteria
articleTitle: SplitCriteria
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété SplitOptions SplitCriteria améliore la gestion des documents en divisant efficacement votre contenu en sections gérables.
type: docs
weight: 20
url: /fr/net/aspose.words.lowcode/splitoptions/splitcriteria/
---
## SplitOptions.SplitCriteria property

Spécifie les critères de division du document en parties.

```csharp
public SplitCriteria SplitCriteria { get; set; }
```

## Exemples

Montre comment diviser un document par pages.

```csharp
string doc = MyDir + "Big document.docx";

SplitOptions options = new SplitOptions();
options.SplitCriteria = SplitCriteria.Page;
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.1.docx", options);
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.2.docx", SaveFormat.Docx, options);
```

### Voir également

* enum [SplitCriteria](../../splitcriteria/)
* class [SplitOptions](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)
