---
title: Document.RevisionsView
second_title: Référence de l'API Aspose.Words pour .NET
description: Document propriété. Obtient ou définit une valeur indiquant sil faut travailler avec la version originale ou révisée dun document.
type: docs
weight: 340
url: /fr/net/aspose.words/document/revisionsview/
---
## Document.RevisionsView property

Obtient ou définit une valeur indiquant s'il faut travailler avec la version originale ou révisée d'un document.

```csharp
public RevisionsView RevisionsView { get; set; }
```

### Remarques

La valeur par défaut est .

### Exemples

Montre comment basculer entre la vue révisée et la vue d'origine d'un document.

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

* enum [RevisionsView](../../revisionsview/)
* class [Document](../)
* espace de noms [Aspose.Words](../../document/)
* Assemblée [Aspose.Words](../../../)


