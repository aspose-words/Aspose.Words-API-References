---
title: Paragraph.IsMoveToRevision
second_title: Référence de l'API Aspose.Words pour .NET
description: Paragraph propriété. Retours vrai si cet objet a été déplacé inséré dans Microsoft Word alors que le suivi des modifications était activé.
type: docs
weight: 140
url: /fr/net/aspose.words/paragraph/ismovetorevision/
---
## Paragraph.IsMoveToRevision property

Retours **vrai** si cet objet a été déplacé (inséré) dans Microsoft Word alors que le suivi des modifications était activé.

```csharp
public bool IsMoveToRevision { get; }
```

### Exemples

Montre comment vérifier si un paragraphe est une révision de déplacement.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// Ce document contient des révisions "Déplacer", qui apparaissent lorsque l'on surligne du texte avec le curseur,
// puis faites-le glisser pour le déplacer vers un autre emplacement
// lors du suivi des révisions dans Microsoft Word via "Review" -> "Suivi des modifications".
Assert.AreEqual(6, doc.Revisions.Count(r => r.RevisionType == RevisionType.Moving));

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

// Les révisions de déplacement consistent en des paires de révisions "Déplacer de" et "Déplacer vers". 
// Ces révisions sont des modifications potentielles du document que nous pouvons accepter ou rejeter.
// Avant d'accepter/rejeter une révision de déplacement, le document
// doit garder une trace des destinations de départ et d'arrivée du texte.
// Le deuxième et le quatrième paragraphe définissent une telle révision, et donc les deux ont le même contenu.
Assert.AreEqual(paragraphs[1].GetText(), paragraphs[3].GetText());

// La révision "Move from" est le paragraphe d'où nous avons fait glisser le texte.
// Si nous acceptons la révision, ce paragraphe disparaîtra,
// et l'autre restera et ne sera plus une révision.
Assert.True(paragraphs[1].IsMoveFromRevision);

// La révision "Déplacer vers" est le paragraphe vers lequel nous avons fait glisser le texte.
// Si nous rejetons la révision, ce paragraphe disparaîtra à la place, et l'autre restera.
Assert.True(paragraphs[3].IsMoveToRevision);
```

### Voir également

* class [Paragraph](../)
* espace de noms [Aspose.Words](../../paragraph/)
* Assemblée [Aspose.Words](../../../)


