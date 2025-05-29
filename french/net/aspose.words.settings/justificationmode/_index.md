---
title: JustificationMode Enum
linktitle: JustificationMode
articleTitle: JustificationMode
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words JustificationMode pour ajuster précisément l'espacement des caractères dans vos documents. Améliorez la lisibilité grâce à des paramètres personnalisables !
type: docs
weight: 6630
url: /fr/net/aspose.words.settings/justificationmode/
---
## JustificationMode enumeration

Spécifie l'ajustement de l'espacement des caractères pour un document. La valeur par défaut est`Développer` .

```csharp
public enum JustificationMode
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Expand | `0` | Ne compressez pas l'espacement des caractères. |
| Compress | `1` | Compresser l'espacement des caractères. |
| CompressKana | `2` | Compresser en utilisant les règles des syllabaires kana, Hiragana et Katakana. |

## Exemples

Montre comment gérer le contrôle de l'espacement des caractères.

```csharp
Document doc = new Document(MyDir + "Document.docx");

JustificationMode justificationMode = doc.JustificationMode;
if (justificationMode == JustificationMode.Expand)
    doc.JustificationMode = JustificationMode.Compress;

doc.Save(ArtifactsDir + "Document.SetJustificationMode.docx");
```

### Voir également

* espace de noms [Aspose.Words.Settings](../../aspose.words.settings/)
* Assemblée [Aspose.Words](../../)
