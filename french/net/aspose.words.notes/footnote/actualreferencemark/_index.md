---
title: Footnote.ActualReferenceMark
linktitle: ActualReferenceMark
articleTitle: ActualReferenceMark
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Footnote ActualReferenceMark pour accéder au texte précis des marques de référence dans vos documents, améliorant ainsi la clarté et l'organisation.
type: docs
weight: 20
url: /fr/net/aspose.words.notes/footnote/actualreferencemark/
---
## Footnote.ActualReferenceMark property

Obtient le texte réel de la marque de référence affichée dans le document pour cette note de bas de page.

```csharp
public string ActualReferenceMark { get; }
```

## Remarques

Pour renseigner initialement les valeurs de cette propriété pour toutes les marques de référence du document, ou pour mettre à jour les valeurs après des modifications dans le document qui pourraient affecter les marques de référence, vous devez exécuter la commande [`UpdateActualReferenceMarks`](../../../aspose.words/document/updateactualreferencemarks/) méthode. Mise à jour des champs ([`UpdateFields`](../../../aspose.words/document/updatefields/) ) peut également être nécessaire pour obtenir le résultat correct.

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

* class [Footnote](../)
* espace de noms [Aspose.Words.Notes](../../../aspose.words.notes/)
* Assemblée [Aspose.Words](../../../)
