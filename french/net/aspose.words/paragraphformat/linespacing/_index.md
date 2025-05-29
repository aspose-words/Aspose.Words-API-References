---
title: ParagraphFormat.LineSpacing
linktitle: LineSpacing
articleTitle: LineSpacing
second_title: Aspose.Words pour .NET
description: Ajustez facilement l'interligne de vos paragraphes grâce à la propriété ParagraphFormat LineSpacing. Améliorez la lisibilité et le style de vos documents !
type: docs
weight: 190
url: /fr/net/aspose.words/paragraphformat/linespacing/
---
## ParagraphFormat.LineSpacing property

Obtient ou définit l'interligne (en points) du paragraphe.

```csharp
public double LineSpacing { get; set; }
```

## Remarques

Quand[`LineSpacingRule`](../linespacingrule/) la propriété est définie surAtLeast , l'espacement des lignes peut être supérieur ou égal à, mais jamais inférieur à celui spécifié`LineSpacing` valeur.

Quand[`LineSpacingRule`](../linespacingrule/) la propriété est définie surExactly , l'espacement des lignes ne change jamais de le spécifié`LineSpacing` valeur, même si une police plus grande est utilisée dans le paragraphe.

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

* class [ParagraphFormat](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
