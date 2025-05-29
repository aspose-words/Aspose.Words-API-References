---
title: FootnoteSeparatorType Enum
linktitle: FootnoteSeparatorType
articleTitle: FootnoteSeparatorType
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.FootnoteSeparatorType pour personnaliser les séparateurs de notes de bas de page et de fin, améliorant ainsi la mise en forme et la lisibilité du document.
type: docs
weight: 5010
url: /fr/net/aspose.words.notes/footnoteseparatortype/
---
## FootnoteSeparatorType enumeration

Spécifie le type de séparateur de note de bas de page/note de fin.

```csharp
public enum FootnoteSeparatorType
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| FootnoteSeparator | `0` | Séparateur entre le texte principal et le texte de la note de bas de page. |
| FootnoteContinuationSeparator | `1` | Imprimé au-dessus du texte de note de bas de page sur une page lorsque le texte doit être continué à partir d'une page précédente. |
| FootnoteContinuationNotice | `2` | Imprimé sous le texte de la note de bas de page sur une page lorsque le texte de la note de bas de page doit être continué sur une page suivante. |
| EndnoteSeparator | `3` | Séparateur entre le texte principal et le texte de la note de fin. |
| EndnoteContinuationSeparator | `4` | Imprimé au-dessus du texte de note de fin de page lorsque le texte doit être continué à partir d'une page précédente. |
| EndnoteContinuationNotice | `5` | Imprimé sous le texte de la note de fin d'une page lorsque le texte de la note de fin doit être continué sur une page suivante. |

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

* espace de noms [Aspose.Words.Notes](../../aspose.words.notes/)
* Assemblée [Aspose.Words](../../)
