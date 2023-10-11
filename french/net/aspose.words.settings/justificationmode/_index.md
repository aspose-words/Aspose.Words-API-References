---
title: Enum JustificationMode
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Settings.JustificationMode énumération. Spécifie lajustement de lespacement des caractères pour un document. La valeur par défaut estDévelopper .
type: docs
weight: 5800
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
| Expand | `0` |  |
| Compress | `1` |  |
| CompressKana | `2` |  |

### Exemples

Montre comment gérer le contrôle de l’espacement des caractères.

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


