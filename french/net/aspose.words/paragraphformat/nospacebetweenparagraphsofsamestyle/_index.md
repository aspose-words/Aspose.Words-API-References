---
title: ParagraphFormat.NoSpaceBetweenParagraphsOfSameStyle
second_title: Référence de l'API Aspose.Words pour .NET
description: ParagraphFormat propriété. Quandvrai SpaceBefore etSpaceAfter sera ignoré entre les paragraphes du même style.
type: docs
weight: 240
url: /fr/net/aspose.words/paragraphformat/nospacebetweenparagraphsofsamestyle/
---
## ParagraphFormat.NoSpaceBetweenParagraphsOfSameStyle property

Quand`vrai` ,[`SpaceBefore`](../spacebefore/) et[`SpaceAfter`](../spaceafter/) sera ignoré entre les paragraphes du même style.

```csharp
public bool NoSpaceBetweenParagraphsOfSameStyle { get; set; }
```

### Remarques

Ce paramètre ne prend effet que lorsqu'il est appliqué à un style de paragraphe. S'il est appliqué directement à un paragraphe, cela n'a aucun effet.

### Exemples

Montre comment n’appliquer aucun espacement entre les paragraphes ayant le même style.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Applique une grande quantité d'espacement avant et après les paragraphes que ce générateur créera.
builder.ParagraphFormat.SpaceBefore = 24;
builder.ParagraphFormat.SpaceAfter = 24;

// Définissez l'indicateur "NoSpaceBetweenParagraphsOfSameStyle" sur "true" pour appliquer
// pas d'espacement entre les paragraphes de même style, ce qui regroupera les paragraphes similaires.
// Laisse le flag "NoSpaceBetweenParagraphsOfSameStyle" à "false"
// pour appliquer uniformément un espacement à chaque paragraphe.
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
* espace de noms [Aspose.Words](../../paragraphformat/)
* Assemblée [Aspose.Words](../../../)


