---
title: Footnote.ReferenceMark
linktitle: ReferenceMark
articleTitle: ReferenceMark
second_title: Aspose.Words pour .NET
description: Personnalisez vos notes de bas de page avec la propriété ReferenceMark. Définissez facilement des marqueurs uniques pour plus de clarté et d'organisation dans vos documents. Améliorez la lisibilité dès aujourd'hui !
type: docs
weight: 60
url: /fr/net/aspose.words.notes/footnote/referencemark/
---
## Footnote.ReferenceMark property

Obtient/définit la marque de référence personnalisée à utiliser pour cette note de bas de page. La valeur par défaut est**chaîne vide** (Empty ), ce qui signifie que des notes de bas de page numérotées automatiquement sont utilisées.

```csharp
public string ReferenceMark { get; set; }
```

## Remarques

Si cette propriété est définie sur**chaîne vide** (Empty ) ou`nul` , alors[`IsAuto`](../isauto/) la propriété sera automatiquement définie sur`vrai` , si défini sur autre chose alors[`IsAuto`](../isauto/) sera réglé sur`FAUX` .

Le format RTF ne peut stocker qu'un seul symbole comme marque de référence personnalisée, donc lors de l'exportation, seul le premier symbole sera écrit, les autres seront ignorés.

## Exemples

Montre comment insérer et personnaliser des notes de bas de page.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ajoutez du texte et référencez-le par une note de bas de page. Cette note placera une petite référence en exposant.
// marquez après le texte auquel il fait référence et créez une entrée sous le texte principal au bas de la page.
// Cette entrée contiendra la marque de référence de la note de bas de page et le texte de référence,
// que nous transmettrons à la méthode « InsertFootnote » du générateur de documents.
builder.Write("Main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Si cette propriété est définie sur « true », alors la marque de référence de notre note de bas de page
// sera son index parmi toutes les notes de bas de page de la section.
// Ceci est la première note de bas de page, donc la marque de référence sera « 1 ».
Assert.True(footnote.IsAuto);

 // Nous pouvons déplacer le générateur de documents à l'intérieur de la note de bas de page pour modifier son texte de référence.
builder.MoveTo(footnote.FirstParagraph);
builder.Write(" More text added by a DocumentBuilder.");
builder.MoveToDocumentEnd();

Assert.AreEqual("\u0002 Footnote text. More text added by a DocumentBuilder.", footnote.GetText().Trim());

builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Nous pouvons définir une marque de référence personnalisée que la note de bas de page utilisera à la place de son numéro d'index.
footnote.ReferenceMark = "RefMark";

Assert.False(footnote.IsAuto);

// Un signet avec l'indicateur « IsAuto » défini sur vrai affichera toujours son index réel
// même si les signets précédents affichent des marques de référence personnalisées, la marque de référence de ce signet sera un « 3 ».
builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

Assert.True(footnote.IsAuto);

doc.Save(ArtifactsDir + "InlineStory.AddFootnote.docx");
```

### Voir également

* class [Footnote](../)
* espace de noms [Aspose.Words.Notes](../../../aspose.words.notes/)
* Assemblée [Aspose.Words](../../../)
