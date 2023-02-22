---
title: ParagraphFormat.SpaceAfter
second_title: Référence de l'API Aspose.Words pour .NET
description: ParagraphFormat propriété. Obtient ou définit la quantité despacement en points après le paragraphe.
type: docs
weight: 290
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
| ArgumentOutOfRangeException | Lance lorsque l'argument est en dehors de la plage de valeurs valides. |

### Remarques

N'a aucun effet lorsque[`SpaceAfterAuto`](../spaceafterauto/) est vrai.

Les valeurs valides vont de 0 à 1584 inclus.

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

Montre comment appliquer aucun espacement entre les paragraphes avec le même style.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Appliquez une grande quantité d'espacement avant et après les paragraphes que ce constructeur va créer.
builder.ParagraphFormat.SpaceBefore = 24;
builder.ParagraphFormat.SpaceAfter = 24;

// Définissez le drapeau "NoSpaceBetweenParagraphsOfSameStyle" sur "true" pour appliquer
// pas d'espacement entre les paragraphes de même style, ce qui regroupera les paragraphes similaires.
// Laisse le drapeau "NoSpaceBetweenParagraphsOfSameStyle" sur "false"
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
* espace de noms [Aspose.Words](../../paragraphformat/)
* Assemblée [Aspose.Words](../../../)


