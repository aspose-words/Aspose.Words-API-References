---
title: Underline Enum
linktitle: Underline
articleTitle: Underline
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Underline pour des options polyvalentes de soulignement des polices. Améliorez la mise en forme de vos documents avec des styles personnalisables dès aujourd'hui !
type: docs
weight: 7360
url: /fr/net/aspose.words/underline/
---
## Underline enumeration

Indique le type de soulignement appliqué à une police.

```csharp
public enum Underline
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| None | `0` |  |
| Single | `1` |  |
| Words | `2` |  |
| Double | `3` |  |
| Dotted | `4` |  |
| Thick | `6` |  |
| Dash | `7` |  |
| DashLong | `39` |  |
| DotDash | `9` |  |
| DotDotDash | `10` |  |
| Wavy | `11` |  |
| DottedHeavy | `20` |  |
| DashHeavy | `23` |  |
| DashLongHeavy | `55` |  |
| DotDashHeavy | `25` |  |
| DotDotDashHeavy | `26` |  |
| WavyHeavy | `27` |  |
| WavyDouble | `43` |  |

## Exemples

Montre comment insérer un champ d'hyperlien.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("For more information, please visit the ");

// Insérez un lien hypertexte et mettez-le en valeur avec une mise en forme personnalisée.
// L'hyperlien sera un morceau de texte cliquable qui nous mènera à l'emplacement spécifié dans l'URL.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Google website", "https://www.google.com", faux);
builder.Font.ClearFormatting();
builder.Writeln(".");

// Ctrl + clic gauche sur le lien dans le texte dans Microsoft Word nous amènera à l'URL via une nouvelle fenêtre de navigateur Web.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlink.docx");
```

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
