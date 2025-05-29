---
title: FootnoteSeparatorCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words pour .NET
description: Accédez à la propriété d'élément FootnoteSeparatorCollection pour récupérer facilement des FootnoteSeparators personnalisés par type, améliorant ainsi la mise en forme de votre document.
type: docs
weight: 20
url: /fr/net/aspose.words.notes/footnoteseparatorcollection/item/
---
## FootnoteSeparatorCollection indexer

Récupère un[`FootnoteSeparator`](../../footnoteseparator/) du type spécifié.

```csharp
public FootnoteSeparator this[FootnoteSeparatorType separatorType] { get; }
```

## Remarques

Retours`nul` si le séparateur de note de bas de page/note de fin du type spécifié n'est pas trouvé.

## Exemples

Montre comment gérer le format du séparateur de notes de bas de page.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

FootnoteSeparator footnoteSeparator = doc.FootnoteSeparators[FootnoteSeparatorType.FootnoteSeparator];
// Aligner le séparateur de notes de bas de page.
footnoteSeparator.FirstParagraph.ParagraphFormat.Alignment = ParagraphAlignment.Center;
```

### Voir également

* class [FootnoteSeparator](../../footnoteseparator/)
* enum [FootnoteSeparatorType](../../footnoteseparatortype/)
* class [FootnoteSeparatorCollection](../)
* espace de noms [Aspose.Words.Notes](../../../aspose.words.notes/)
* Assemblée [Aspose.Words](../../../)
