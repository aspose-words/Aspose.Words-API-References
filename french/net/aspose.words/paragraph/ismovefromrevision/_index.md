---
title: Paragraph.IsMoveFromRevision
linktitle: IsMoveFromRevision
articleTitle: IsMoveFromRevision
second_title: Aspose.Words pour .NET
description: Paragraph IsMoveFromRevision propriété. Retoursvrai si cet objet a été déplacé supprimé dans Microsoft Word alors que le suivi des modifications était activé en C#.
type: docs
weight: 130
url: /fr/net/aspose.words/paragraph/ismovefromrevision/
---
## Paragraph.IsMoveFromRevision property

Retours`vrai` si cet objet a été déplacé (supprimé) dans Microsoft Word alors que le suivi des modifications était activé.

```csharp
public bool IsMoveFromRevision { get; }
```

## Exemples

Montre comment vérifier si un paragraphe est une révision de déplacement.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// Ce document contient des révisions "Déplacer", qui apparaissent lorsque l'on surligne du texte avec le curseur,
// puis faites-le glisser pour le déplacer vers un autre emplacement
// lors du suivi des révisions dans Microsoft Word via "Review" -> "Suivi des modifications".
Assert.AreEqual(6, doc.Revisions.Count(r => r.RevisionType == RevisionType.Moving));

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

 // Les révisions de déplacement sont constituées de paires de révisions « Déplacer de » et « Déplacer vers ».
// Ces révisions sont des modifications potentielles du document que nous pouvons accepter ou rejeter.
// Avant d'accepter/rejeter une révision de déplacement, le document
// doit garder une trace des destinations de départ et d'arrivée du texte.
// Les deuxième et quatrième paragraphes définissent une de ces révisions et ont donc tous deux le même contenu.
Assert.AreEqual(paragraphs[1].GetText(), paragraphs[3].GetText());

// La révision "Déplacer depuis" est le paragraphe à partir duquel nous avons fait glisser le texte.
// Si nous acceptons la révision, ce paragraphe disparaîtra,
// et l'autre resteront et ne seront plus une révision.
Assert.True(paragraphs[1].IsMoveFromRevision);

// La révision "Déplacer vers" est le paragraphe vers lequel nous avons fait glisser le texte.
// Si nous rejetons la révision, ce paragraphe disparaîtra et l'autre restera.
Assert.True(paragraphs[3].IsMoveToRevision);
```

### Voir également

* class [Paragraph](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
