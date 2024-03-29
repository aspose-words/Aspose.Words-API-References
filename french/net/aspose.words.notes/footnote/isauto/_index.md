---
title: Footnote.IsAuto
linktitle: IsAuto
articleTitle: IsAuto
second_title: Aspose.Words pour .NET
description: Footnote IsAuto propriété. Contient une valeur qui spécifie sil sagit dune note de bas de page numérotée automatiquement ou dune note de bas de page avec une marque de référence personnalisée définie par lutilisateur en C#.
type: docs
weight: 30
url: /fr/net/aspose.words.notes/footnote/isauto/
---
## Footnote.IsAuto property

Contient une valeur qui spécifie s'il s'agit d'une note de bas de page numérotée automatiquement ou d'une note de bas de page avec une marque de référence personnalisée définie par l'utilisateur.

```csharp
public bool IsAuto { get; set; }
```

## Remarques

[`ReferenceMark`](../referencemark/)initialisé avec une chaîne vide si`IsAuto` mis à`FAUX` .

## Exemples

Montre comment insérer et personnaliser des notes de bas de page.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ajoutez du texte et référencez-le avec une note de bas de page. Cette note de bas de page placera une petite référence en exposant
// marque après le texte auquel il fait référence et crée une entrée sous le corps du texte principal en bas de la page.
// Cette entrée contiendra la marque de référence de la note de bas de page et le texte de référence,
// que nous transmettrons à la méthode "InsertFootnote" du générateur de documents.
builder.Write("Main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Si cette propriété est définie sur "true", alors la marque de référence de notre note de bas de page
// sera son index parmi toutes les notes de bas de page de la section.
// Ceci est la première note de bas de page, donc la marque de référence sera "1".
Assert.True(footnote.IsAuto);

 // Nous pouvons déplacer le générateur de document à l'intérieur de la note de bas de page pour modifier son texte de référence.
builder.MoveTo(footnote.FirstParagraph);
builder.Write(" More text added by a DocumentBuilder.");
builder.MoveToDocumentEnd();

Assert.AreEqual("\u0002 Footnote text. More text added by a DocumentBuilder.", footnote.GetText().Trim());

builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Nous pouvons définir une marque de référence personnalisée que la note de bas de page utilisera à la place de son numéro d'index.
footnote.ReferenceMark = "RefMark";

Assert.False(footnote.IsAuto);

// Un signet avec l'indicateur "IsAuto" défini sur true affichera toujours son véritable index
// même si les signets précédents affichent des marques de référence personnalisées, la marque de référence de ce signet sera donc un "3".
builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

Assert.True(footnote.IsAuto);

doc.Save(ArtifactsDir + "InlineStory.AddFootnote.docx");
```

### Voir également

* class [Footnote](../)
* espace de noms [Aspose.Words.Notes](../../../aspose.words.notes/)
* Assemblée [Aspose.Words](../../../)
