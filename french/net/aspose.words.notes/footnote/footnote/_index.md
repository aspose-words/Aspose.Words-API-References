---
title: Footnote
linktitle: Footnote
articleTitle: Footnote
second_title: Aspose.Words pour .NET
description: Créez facilement des notes de bas de page attrayantes grâce à notre outil de création de notes de bas de page. Améliorez la clarté et le professionnalisme de votre contenu en quelques clics !
type: docs
weight: 10
url: /fr/net/aspose.words.notes/footnote/footnote/
---
## Footnote constructor

Initialise une instance du[`Footnote`](../) classe.

```csharp
public Footnote(DocumentBase doc, FootnoteType footnoteType)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| doc | DocumentBase | Le document du propriétaire. |
| footnoteType | FootnoteType | UN[`FootnoteType`](../footnotetype/) value qui spécifie s'il s'agit d'une note de bas de page ou d'une note de fin. |

## Remarques

Quand[`Footnote`](../) est créé, il appartient au document spécifié, mais ne fait pas encore partie du document et[`ParentNode`](../../../aspose.words/node/parentnode/) est`nul`.

Pour ajouter[`Footnote`](../) à l'utilisation du document[`InsertAfter`](../../../aspose.words/compositenode/insertafter/) ou[`InsertBefore`](../../../aspose.words/compositenode/insertbefore/) sur le paragraphe où vous souhaitez insérer la note de bas de page.

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

* class [DocumentBase](../../../aspose.words/documentbase/)
* enum [FootnoteType](../../footnotetype/)
* class [Footnote](../)
* espace de noms [Aspose.Words.Notes](../../../aspose.words.notes/)
* Assemblée [Aspose.Words](../../../)
