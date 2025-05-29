---
title: IStructuredDocumentTag.RemoveSelfOnly
linktitle: RemoveSelfOnly
articleTitle: RemoveSelfOnly
second_title: Aspose.Words pour .NET
description: Découvrez la méthode IStructuredDocumentTag RemoveSelfOnly pour supprimer sans effort un nœud SDT tout en préservant son contenu dans votre arborescence de documents.
type: docs
weight: 180
url: /fr/net/aspose.words.markup/istructureddocumenttag/removeselfonly/
---
## IStructuredDocumentTag.RemoveSelfOnly method

Supprime uniquement ce nœud SDT lui-même, mais conserve son contenu dans l'arborescence du document.

```csharp
public void RemoveSelfOnly()
```

## Exemples

Montre comment supprimer la balise de document structuré, mais conserve le contenu à l'intérieur.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

 // Cette collection fournit une interface unifiée pour accéder aux balises structurées à distance et sans distance.
IEnumerable<IStructuredDocumentTag> sdts = doc.Range.StructuredDocumentTags.ToList();
Assert.AreEqual(5, sdts.Count());

// Ici, nous pouvons obtenir des nœuds enfants à partir de l'interface commune des balises structurées à distance et sans distance.
foreach (IStructuredDocumentTag sdt in sdts)
    if (sdt.GetChildNodes(NodeType.Any, false).Count > 0)
        sdt.RemoveSelfOnly();

sdts = doc.Range.StructuredDocumentTags.ToList();
Assert.AreEqual(0, sdts.Count());
```

### Voir également

* interface [IStructuredDocumentTag](../)
* espace de noms [Aspose.Words.Markup](../../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../../)
