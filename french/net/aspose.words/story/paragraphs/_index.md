---
title: Story.Paragraphs
linktitle: Paragraphs
articleTitle: Paragraphs
second_title: Aspose.Words pour .NET
description: Découvrez les paragraphes de votre histoire. Accédez à une collection de paragraphes sélectionnés directement de votre histoire, enrichissant votre récit d'un contenu riche et captivant.
type: docs
weight: 30
url: /fr/net/aspose.words/story/paragraphs/
---
## Story.Paragraphs property

Obtient une collection de paragraphes qui sont les enfants immédiats de l'histoire.

```csharp
public ParagraphCollection Paragraphs { get; }
```

## Exemples

Montre comment vérifier si un paragraphe est une révision de déplacement.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// Ce document contient des révisions « Déplacer », qui apparaissent lorsque nous mettons en surbrillance du texte avec le curseur,
// puis faites-le glisser pour le déplacer vers un autre emplacement
// lors du suivi des révisions dans Microsoft Word via « Révision » -> « Suivre les modifications ».
Assert.AreEqual(6, doc.Revisions.Count(r => r.RevisionType == RevisionType.Moving));

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

 // Les révisions de déplacement se composent de paires de révisions « Déplacer de » et « Déplacer vers ».
// Ces révisions sont des modifications potentielles du document que nous pouvons accepter ou rejeter.
// Avant d'accepter/rejeter une révision de déplacement, le document
// doit garder une trace des destinations de départ et d'arrivée du texte.
// Le deuxième et le quatrième paragraphe définissent une telle révision et ont donc tous deux le même contenu.
Assert.AreEqual(paragraphs[1].GetText(), paragraphs[3].GetText());

// La révision « Déplacer depuis » est le paragraphe à partir duquel nous avons fait glisser le texte.
// Si nous acceptons la révision, ce paragraphe disparaîtra,
// et l'autre restera et ne sera plus une révision.
Assert.True(paragraphs[1].IsMoveFromRevision);

// La révision « Déplacer vers » est le paragraphe vers lequel nous avons fait glisser le texte.
// Si nous rejetons la révision, ce paragraphe disparaîtra et l'autre restera.
Assert.True(paragraphs[3].IsMoveToRevision);
```

### Voir également

* class [ParagraphCollection](../../paragraphcollection/)
* class [Story](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
