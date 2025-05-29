---
title: FootnoteSeparatorCollection Class
linktitle: FootnoteSeparatorCollection
articleTitle: FootnoteSeparatorCollection
second_title: Aspose.Words pour .NET
description: Découvrez Aspose.Words.Notes.FootnoteSeparatorCollection pour accéder facilement aux séparateurs de notes de bas de page dans vos documents. Améliorez la mise en forme de vos documents dès aujourd'hui !
type: docs
weight: 5000
url: /fr/net/aspose.words.notes/footnoteseparatorcollection/
---
## FootnoteSeparatorCollection class

Fournit un accès typé à[`FootnoteSeparator`](../footnoteseparator/) nœuds d'un document.

```csharp
public class FootnoteSeparatorCollection : IEnumerable<FootnoteSeparator>
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [FootnoteSeparatorCollection](footnoteseparatorcollection/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [Item](../../aspose.words.notes/footnoteseparatorcollection/item/) { get; } | Récupère un[`FootnoteSeparator`](../footnoteseparator/) du type spécifié. |

## Méthodes

| Nom | La description |
| --- | --- |
| [GetEnumerator](../../aspose.words.notes/footnoteseparatorcollection/getenumerator/)() |  |

## Exemples

Montre comment gérer le format du séparateur de notes de bas de page.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

FootnoteSeparator footnoteSeparator = doc.FootnoteSeparators[FootnoteSeparatorType.FootnoteSeparator];
// Aligner le séparateur de notes de bas de page.
footnoteSeparator.FirstParagraph.ParagraphFormat.Alignment = ParagraphAlignment.Center;
```

### Voir également

* class [FootnoteSeparator](../footnoteseparator/)
* espace de noms [Aspose.Words.Notes](../../aspose.words.notes/)
* Assemblée [Aspose.Words](../../)
