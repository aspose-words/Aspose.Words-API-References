---
title: DocumentBase.FootnoteSeparators
linktitle: FootnoteSeparators
articleTitle: FootnoteSeparators
second_title: Aspose.Words pour .NET
description: Accédez et personnalisez les séparateurs de notes de bas de page et de fin de document avec la propriété FootnoteSeparators de DocumentBase pour un contrôle de mise en forme amélioré.
type: docs
weight: 40
url: /fr/net/aspose.words/documentbase/footnoteseparators/
---
## DocumentBase.FootnoteSeparators property

Donne accès aux séparateurs de notes de bas de page/de fin définis dans le document.

```csharp
public FootnoteSeparatorCollection FootnoteSeparators { get; }
```

## Exemples

Montre comment supprimer le séparateur de note de fin.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

FootnoteSeparator endnoteSeparator = doc.FootnoteSeparators[FootnoteSeparatorType.EndnoteSeparator];
// Supprimer le séparateur de note de fin.
endnoteSeparator.FirstParagraph.FirstChild.Remove();
```

Montre comment gérer le format du séparateur de notes de bas de page.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

FootnoteSeparator footnoteSeparator = doc.FootnoteSeparators[FootnoteSeparatorType.FootnoteSeparator];
// Aligner le séparateur de notes de bas de page.
footnoteSeparator.FirstParagraph.ParagraphFormat.Alignment = ParagraphAlignment.Center;
```

### Voir également

* class [FootnoteSeparatorCollection](../../../aspose.words.notes/footnoteseparatorcollection/)
* class [DocumentBase](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
