---
title: LineSpacingRule Enum
linktitle: LineSpacingRule
articleTitle: LineSpacingRule
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.LineSpacingRule pour personnaliser l'espacement des paragraphes. Améliorez la mise en forme de vos documents grâce à un contrôle précis et une meilleure lisibilité.
type: docs
weight: 3890
url: /fr/net/aspose.words/linespacingrule/
---
## LineSpacingRule enumeration

Spécifie les valeurs d'espacement des lignes pour un paragraphe.

```csharp
public enum LineSpacingRule
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| AtLeast | `0` | L'interligne peut être supérieur ou égal, mais jamais inférieur, à la valeur spécifiée dans le[`LineSpacing`](../paragraphformat/linespacing/) propriété. |
| Exactly | `1` | L'espacement des lignes ne change jamais par rapport à la valeur spécifiée dans le [`LineSpacing`](../paragraphformat/linespacing/) propriété, même si une police plus grande est utilisée dans le paragraphe. |
| Multiple | `2` | L'espacement des lignes est spécifié dans le[`LineSpacing`](../paragraphformat/linespacing/) Propriété : nombre de lignes. Une ligne équivaut à 12 points. |

## Exemples

Montre comment travailler avec l'espacement des lignes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Vous trouverez ci-dessous trois règles d'espacement des lignes que nous pouvons définir à l'aide de
// propriété « LineSpacingRule » du paragraphe pour configurer l'espacement entre les paragraphes.
// 1 - Définir une quantité minimale d'espacement.
// Cela donnera un remplissage vertical aux lignes de texte de n'importe quelle taille
// qui est trop petit pour maintenir la hauteur de ligne minimale.
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.AtLeast;
builder.ParagraphFormat.LineSpacing = 20;

builder.Writeln("Minimum line spacing of 20.");
builder.Writeln("Minimum line spacing of 20.");

// 2 - Définir l'espacement exact.
// L'utilisation de tailles de police trop grandes pour l'espacement tronquera le texte.
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.Exactly;
builder.ParagraphFormat.LineSpacing = 5;

builder.Writeln("Line spacing of exactly 5.");
builder.Writeln("Line spacing of exactly 5.");

// 3 - Définissez l'espacement comme un multiple de l'espacement de ligne par défaut, qui est de 12 points par défaut.
// Ce type d'espacement s'adaptera à différentes tailles de police.
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.Multiple;
builder.ParagraphFormat.LineSpacing = 18;

builder.Writeln("Line spacing of 1.5 default lines.");
builder.Writeln("Line spacing of 1.5 default lines.");

doc.Save(ArtifactsDir + "ParagraphFormat.LineSpacing.docx");
```

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
