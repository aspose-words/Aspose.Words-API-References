---
title: ParagraphFormat.SpaceAfterAuto
second_title: Référence de l'API Aspose.Words pour .NET
description: ParagraphFormat propriété. Vrai si lespacement après le paragraphe est défini automatiquement.
type: docs
weight: 300
url: /fr/net/aspose.words/paragraphformat/spaceafterauto/
---
## ParagraphFormat.SpaceAfterAuto property

Vrai si l'espacement après le paragraphe est défini automatiquement.

```csharp
public bool SpaceAfterAuto { get; set; }
```

### Remarques

Lorsqu'il est défini sur true, remplace l'effet de[`SpaceAfter`](../spaceafter/).

Lorsque vous définissez Espace avant et Espace après les paragraphes sur Auto, Microsoft Word ajoute automatiquement un espacement de 14 points entre les paragraphes selon les règles suivantes :

* Normalement, un espacement est ajouté après tous les paragraphes.
* Dans une liste à puces ou numérotée, l'espacement n'est ajouté qu'après le dernier élément de la liste. L'espacement n'est pas ajouté entre les éléments de la liste.
* Dans une liste imbriquée à puces ou numérotée, l'espacement n'est pas ajouté.
* L'espacement est normalement ajouté après un tableau.
* L'espacement n'est pas ajouté après un tableau s'il s'agit du dernier bloc d'une cellule de tableau.
* L'espacement n'est pas ajouté après le dernier paragraphe d'une cellule de tableau.

### Exemples

Montre comment définir l'espacement automatique des paragraphes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Appliquez une grande quantité d'espacement avant et après les paragraphes que ce constructeur va créer.
builder.ParagraphFormat.SpaceBefore = 24;
builder.ParagraphFormat.SpaceAfter = 24;

// Définissez ces drapeaux sur "true" pour appliquer un espacement automatique,
// en ignorant effectivement l'espacement dans les propriétés que nous avons définies ci-dessus.
// Laissez-les comme "faux" appliquera notre espacement de paragraphe personnalisé.
builder.ParagraphFormat.SpaceAfterAuto = autoSpacing;
builder.ParagraphFormat.SpaceBeforeAuto = autoSpacing;

// Insérez deux paragraphes qui auront un espacement au-dessus et au-dessous d'eux et enregistrez le document.
builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphSpacingAuto.docx");
```

### Voir également

* class [ParagraphFormat](../)
* espace de noms [Aspose.Words](../../paragraphformat/)
* Assemblée [Aspose.Words](../../../)


