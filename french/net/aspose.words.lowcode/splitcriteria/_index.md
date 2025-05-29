---
title: SplitCriteria Enum
linktitle: SplitCriteria
articleTitle: SplitCriteria
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.LowCode.SplitCriteria pour un fractionnement efficace des documents. Optimisez votre flux de travail grâce à des options polyvalentes pour une gestion fluide des parties.
type: docs
weight: 4400
url: /fr/net/aspose.words.lowcode/splitcriteria/
---
## SplitCriteria enumeration

Spécifie comment le document est divisé en parties.

```csharp
public enum SplitCriteria
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Page | `0` | Spécifie que le document est divisé en pages. |
| SectionBreak | `1` | Spécifie que le document est divisé en parties lors d'un saut de section de n'importe quel type. |
| Style | `2` | Spécifie que le document est divisé en parties dans un paragraphe formaté à l'aide du style spécifié dans[`SplitStyle`](../splitoptions/splitstyle/) . |

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

* espace de noms [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../)
