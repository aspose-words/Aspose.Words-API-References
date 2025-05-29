---
title: AdvancedCompareOptions.IgnoreStoreItemId
linktitle: IgnoreStoreItemId
articleTitle: IgnoreStoreItemId
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété IgnoreStoreItemId d'AdvancedCompareOptions améliore la comparaison de documents en ignorant les différences d'ID StructuredDocumentTag pour une précision améliorée.
type: docs
weight: 30
url: /fr/net/aspose.words.comparing/advancedcompareoptions/ignorestoreitemid/
---
## AdvancedCompareOptions.IgnoreStoreItemId property

Spécifie s'il faut ignorer la différence dans l'ID d'élément de magasin StructuredDocumentTag.

```csharp
public bool IgnoreStoreItemId { get; set; }
```

## Remarques

La valeur par défaut est`FAUX` .

## Exemples

Montre comment comparer SDT avec le même contenu mais un identifiant d'article de magasin différent.

```csharp
Document docA = new Document(MyDir + "Document with SDT 1.docx");
Document docB = new Document(MyDir + "Document with SDT 2.docx");

// Configurez les options pour comparer SDT avec le même contenu mais un identifiant d'élément de magasin différent.
CompareOptions compareOptions = new CompareOptions();
compareOptions.AdvancedOptions.IgnoreStoreItemId = false;

docA.Compare(docB, "user", DateTime.Now, compareOptions);
Assert.AreEqual(8, docA.Revisions.Count);

compareOptions.AdvancedOptions.IgnoreStoreItemId = true;

docA.Revisions.RejectAll();
docA.Compare(docB, "user", DateTime.Now, compareOptions);
Assert.AreEqual(0, docA.Revisions.Count);
```

### Voir également

* class [AdvancedCompareOptions](../)
* espace de noms [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* Assemblée [Aspose.Words](../../../)
