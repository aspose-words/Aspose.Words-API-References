---
title: RevisionsView Enum
linktitle: RevisionsView
articleTitle: RevisionsView
second_title: Aspose.Words pour .NET
description: Aspose.Words.RevisionsView énumération. Permet de spécifier sil faut travailler avec la version originale ou révisée dun document en C#.
type: docs
weight: 4810
url: /fr/net/aspose.words/revisionsview/
---
## RevisionsView enumeration

Permet de spécifier s'il faut travailler avec la version originale ou révisée d'un document.

```csharp
public enum RevisionsView
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Original | `0` | Spécifie la version originale d'un document. |
| Final | `1` | Spécifie la version révisée d'un document. |

## Exemples

Montre comment basculer entre la vue révisée et la vue originale d'un document.

```csharp
Document doc = new Document(MyDir + "Revisions at list levels.docx");
doc.UpdateListLabels();

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;
Assert.AreEqual("1.", paragraphs[0].ListLabel.LabelString);
Assert.AreEqual("a.", paragraphs[1].ListLabel.LabelString);
Assert.AreEqual(string.Empty, paragraphs[2].ListLabel.LabelString);

// Affiche l'objet document comme si toutes les révisions étaient acceptées. Prend actuellement en charge les étiquettes de liste.
doc.RevisionsView = RevisionsView.Final;

Assert.AreEqual(string.Empty, paragraphs[0].ListLabel.LabelString);
Assert.AreEqual("1.", paragraphs[1].ListLabel.LabelString);
Assert.AreEqual("a.", paragraphs[2].ListLabel.LabelString);
```

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
