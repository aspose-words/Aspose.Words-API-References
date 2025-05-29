---
title: Paragraph.BreakIsStyleSeparator
linktitle: BreakIsStyleSeparator
articleTitle: BreakIsStyleSeparator
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété Paragraph Break IsStyleSeparator améliore la mise en forme des documents en autorisant des styles de paragraphe mixtes pour une plus grande flexibilité de conception.
type: docs
weight: 20
url: /fr/net/aspose.words/paragraph/breakisstyleseparator/
---
## Paragraph.BreakIsStyleSeparator property

Vrai si ce saut de paragraphe est un séparateur de style. Un séparateur de style permet à un paragraphe de se composer de parties ayant des styles de paragraphe différents.

```csharp
public bool BreakIsStyleSeparator { get; }
```

## Exemples

Montre comment écrire du texte sur la même ligne qu'un titre de table des matières et le faire ne pas apparaître dans la table des matières.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertTableOfContents("\\o \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// Insérez un paragraphe avec un style que la table des matières reprendra comme entrée.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

// Ces deux chaînes se trouvent dans le même paragraphe et apparaîtront donc sur la même entrée de table des matières.
builder.Write("Heading 1. ");
builder.Write("Will appear in the TOC. ");

// Si nous insérons un séparateur de style, nous pouvons écrire plus de texte dans le même paragraphe
// et utilisez un style différent sans apparaître dans la table des matières.
// Si nous utilisons un style de type titre après le séparateur, nous pouvons dessiner plusieurs entrées de table des matières à partir d'une ligne de texte de document.
builder.InsertStyleSeparator();
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Quote;
builder.Write("Won't appear in the TOC. ");

Assert.True(doc.FirstSection.Body.FirstParagraph.BreakIsStyleSeparator);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Paragraph.BreakIsStyleSeparator.docx");
```

### Voir également

* class [Paragraph](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
