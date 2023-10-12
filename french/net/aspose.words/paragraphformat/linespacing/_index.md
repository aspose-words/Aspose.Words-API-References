---
title: ParagraphFormat.LineSpacing
second_title: Référence de l'API Aspose.Words pour .NET
description: ParagraphFormat propriété. Obtient ou définit lespacement des lignes en points pour le paragraphe.
type: docs
weight: 190
url: /fr/net/aspose.words/paragraphformat/linespacing/
---
## ParagraphFormat.LineSpacing property

Obtient ou définit l'espacement des lignes (en points) pour le paragraphe.

```csharp
public double LineSpacing { get; set; }
```

### Remarques

Quand[`LineSpacingRule`](../linespacingrule/) la propriété est définie surAtLeast , l'interligne peut être supérieur ou égal à, mais jamais inférieur à l'espacement spécifié`LineSpacing` valeur.

Quand[`LineSpacingRule`](../linespacingrule/) la propriété est définie surExactly , l'interligne ne change jamais par rapport à spécifié`LineSpacing` valeur, même si une police plus grande est utilisée dans le paragraphe.

### Exemples

Montre comment utiliser l'espacement des lignes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Vous trouverez ci-dessous trois règles d'espacement des lignes que nous pouvons définir à l'aide de la
// Propriété "LineSpacingRule" du paragraphe pour configurer l'espacement entre les paragraphes.
// 1 - Définit un espacement minimum.
// Cela donnera un remplissage vertical aux lignes de texte de n'importe quelle taille
// c'est trop petit pour maintenir la hauteur de ligne minimale.
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

// 3 - Définissez l'espacement comme un multiple de l'espacement des lignes par défaut, qui est de 12 points par défaut.
// Ce type d'espacement s'adaptera à différentes tailles de police.
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.Multiple;
builder.ParagraphFormat.LineSpacing = 18;

builder.Writeln("Line spacing of 1.5 default lines.");
builder.Writeln("Line spacing of 1.5 default lines.");

doc.Save(ArtifactsDir + "ParagraphFormat.LineSpacing.docx");
```

### Voir également

* class [ParagraphFormat](../)
* espace de noms [Aspose.Words](../../paragraphformat/)
* Assemblée [Aspose.Words](../../../)


