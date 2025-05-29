---
title: Document.UpdateActualReferenceMarks
linktitle: UpdateActualReferenceMarks
articleTitle: UpdateActualReferenceMarks
second_title: Aspose.Words pour .NET
description: Mettez à jour sans effort toutes les notes de bas de page et de fin de votre document avec la méthode Document UpdateActualReferenceMarks, améliorant ainsi la précision et l'efficacité.
type: docs
weight: 800
url: /fr/net/aspose.words/document/updateactualreferencemarks/
---
## Document.UpdateActualReferenceMarks method

Met à jour le[`ActualReferenceMark`](../../../aspose.words.notes/footnote/actualreferencemark/) propriété de toutes les notes de bas de page et de fin du document.

```csharp
public void UpdateActualReferenceMarks()
```

## Remarques

Mise à jour des champs ([`UpdateFields`](../updatefields/) ) peut être nécessaire pour obtenir le résultat correct.

## Exemples

Montre comment obtenir une marque de référence de note de bas de page réelle.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

Footnote footnote = (Footnote)doc.GetChild(NodeType.Footnote, 1, true);
doc.UpdateFields();
doc.UpdateActualReferenceMarks();

Assert.AreEqual("1", footnote.ActualReferenceMark);
```

### Voir également

* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
