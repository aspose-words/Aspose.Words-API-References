---
title: ParagraphFormat.SpaceBeforeAuto
linktitle: SpaceBeforeAuto
articleTitle: SpaceBeforeAuto
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ParagraphFormat SpaceBeforeAuto. Ajustez automatiquement l'espacement des paragraphes pour un rendu soigné et professionnel de vos documents.
type: docs
weight: 340
url: /fr/net/aspose.words/paragraphformat/spacebeforeauto/
---
## ParagraphFormat.SpaceBeforeAuto property

Vrai si la quantité d'espacement avant le paragraphe est définie automatiquement.

```csharp
public bool SpaceBeforeAuto { get; set; }
```

## Remarques

Lorsqu'il est réglé sur`vrai` , annule l'effet de[`SpaceBefore`](../spacebefore/).

Lorsque vous définissez l'espace avant et l'espace après le paragraphe sur Auto, Microsoft Word ajoute automatiquement un espacement de 14 points entre les paragraphes conformément aux règles suivantes :

* Normalement, l'espacement est ajouté après tous les paragraphes.
* Dans une liste à puces ou numérotée, l'espacement est ajouté uniquement après le dernier élément de la liste. L'espacement n'est pas ajouté entre les éléments de la liste.
* Dans une liste à puces ou numérotée imbriquée, l'espacement n'est pas ajouté.
* L'espacement est normalement ajouté après un tableau.
* L'espacement n'est pas ajouté après un tableau s'il s'agit du dernier bloc d'une cellule de tableau.
* L'espacement n'est pas ajouté après le dernier paragraphe d'une cellule de tableau.

## Exemples

Montre comment définir l'espacement automatique des paragraphes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Appliquez une grande quantité d'espacement avant et après les paragraphes que ce générateur créera.
builder.ParagraphFormat.SpaceBefore = 24;
builder.ParagraphFormat.SpaceAfter = 24;

// Définissez ces indicateurs sur « true » pour appliquer l'espacement automatique,
// en ignorant efficacement l'espacement dans les propriétés que nous avons définies ci-dessus.
// Laissez-les sur « false » et notre espacement de paragraphe personnalisé sera appliqué.
builder.ParagraphFormat.SpaceAfterAuto = autoSpacing;
builder.ParagraphFormat.SpaceBeforeAuto = autoSpacing;

// Insérez deux paragraphes qui auront un espacement au-dessus et en dessous d'eux et enregistrez le document.
builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphSpacingAuto.docx");
```

### Voir également

* class [ParagraphFormat](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
