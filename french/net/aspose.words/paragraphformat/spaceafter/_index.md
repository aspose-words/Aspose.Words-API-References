---
title: ParagraphFormat.SpaceAfter
linktitle: SpaceAfter
articleTitle: SpaceAfter
second_title: Aspose.Words pour .NET
description: Contrôlez l'espacement des paragraphes avec la propriété SpaceAfter. Ajustez facilement l'espacement en points pour améliorer la lisibilité et la présentation de votre document.
type: docs
weight: 310
url: /fr/net/aspose.words/paragraphformat/spaceafter/
---
## ParagraphFormat.SpaceAfter property

Obtient ou définit la quantité d'espacement (en points) après le paragraphe.

```csharp
public double SpaceAfter { get; set; }
```

### Exceptions

| exception | condition |
| --- | --- |
| ArgumentOutOfRangeException | Lancé lorsque l'argument est hors de la plage de valeurs valides. |

## Remarques

N'a aucun effet lorsque[`SpaceAfterAuto`](../spaceafterauto/) est`vrai`.

Les valeurs valides vont de 0 à 1584 inclus.

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

Montre comment appliquer aucun espacement entre les paragraphes avec le même style.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Appliquez une grande quantité d'espacement avant et après les paragraphes que ce générateur créera.
builder.ParagraphFormat.SpaceBefore = 24;
builder.ParagraphFormat.SpaceAfter = 24;

// Définissez l'indicateur « NoSpaceBetweenParagraphsOfSameStyle » sur « true » pour appliquer
// pas d'espacement entre les paragraphes avec le même style, ce qui regroupera les paragraphes similaires.
// Laissez l'indicateur « NoSpaceBetweenParagraphsOfSameStyle » sur « false »
// pour appliquer uniformément l'espacement à chaque paragraphe.
builder.ParagraphFormat.NoSpaceBetweenParagraphsOfSameStyle = noSpaceBetweenParagraphsOfSameStyle;

builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.ParagraphFormat.Style = doc.Styles["Quote"];
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphSpacingSameStyle.docx");
```

### Voir également

* class [ParagraphFormat](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
