---
title: ParagraphFormat.SpaceAfterAuto
second_title: Référence de l'API Aspose.Words pour .NET
description: ParagraphFormat propriété. Vrai si la quantité despacement après le paragraphe est définie automatiquement.
type: docs
weight: 310
url: /fr/net/aspose.words/paragraphformat/spaceafterauto/
---
## ParagraphFormat.SpaceAfterAuto property

Vrai si la quantité d'espacement après le paragraphe est définie automatiquement.

```csharp
public bool SpaceAfterAuto { get; set; }
```

### Remarques

Lorsqu'il est réglé sur`vrai` , annule l'effet de[`SpaceAfter`](../spaceafter/).

Lorsque vous définissez le paragraphe Espace avant et Espace après sur Auto, Microsoft Word ajoute automatiquement un espacement de 14 points entre les paragraphes selon les règles suivantes :

* Normalement, un espacement est ajouté après chaque paragraphe.
* Dans une liste à puces ou numérotée, l'espacement est ajouté uniquement après le dernier élément de la liste. L'espacement n'est pas ajouté entre les éléments de la liste.
* Dans une liste à puces ou numérotée imbriquée, l’espacement n’est pas ajouté.
* L'espacement est normalement ajouté après un tableau.
* L'espacement n'est pas ajouté après un tableau s'il s'agit du dernier bloc d'une cellule du tableau.
* L'espacement n'est pas ajouté après le dernier paragraphe d'une cellule de tableau.

### Exemples

Montre comment définir l’espacement automatique des paragraphes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Applique une grande quantité d'espacement avant et après les paragraphes que ce générateur créera.
builder.ParagraphFormat.SpaceBefore = 24;
builder.ParagraphFormat.SpaceAfter = 24;

// Met ces flags à "true" pour appliquer un espacement automatique,
// ignorant effectivement l'espacement dans les propriétés que nous avons définies ci-dessus.
// Les laisser comme "false" appliquera notre espacement de paragraphe personnalisé.
builder.ParagraphFormat.SpaceAfterAuto = autoSpacing;
builder.ParagraphFormat.SpaceBeforeAuto = autoSpacing;

// Insérez deux paragraphes qui auront un espace au-dessus et en dessous d'eux et enregistrez le document.
builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphSpacingAuto.docx");
```

### Voir également

* class [ParagraphFormat](../)
* espace de noms [Aspose.Words](../../paragraphformat/)
* Assemblée [Aspose.Words](../../../)


