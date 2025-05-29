---
title: ParagraphFormat.NoSpaceBetweenParagraphsOfSameStyle
linktitle: NoSpaceBetweenParagraphsOfSameStyle
articleTitle: NoSpaceBetweenParagraphsOfSameStyle
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ParagraphFormat NoSpaceBetweenParagraphsOfSameStyle. Optimisez la mise en page de votre document en supprimant l'espace entre les paragraphes de même style.
type: docs
weight: 250
url: /fr/net/aspose.words/paragraphformat/nospacebetweenparagraphsofsamestyle/
---
## ParagraphFormat.NoSpaceBetweenParagraphsOfSameStyle property

Quand`vrai` ,[`SpaceBefore`](../spacebefore/) et[`SpaceAfter`](../spaceafter/) sera ignoré entre les paragraphes du même style.

```csharp
public bool NoSpaceBetweenParagraphsOfSameStyle { get; set; }
```

## Remarques

Ce paramètre n'est effectif que s'il est appliqué à un style de paragraphe. S'il est appliqué directement à un paragraphe, il n'a aucun effet.

## Exemples

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
