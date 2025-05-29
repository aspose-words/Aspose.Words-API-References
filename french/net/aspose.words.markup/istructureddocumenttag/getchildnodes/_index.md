---
title: IStructuredDocumentTag.GetChildNodes
linktitle: GetChildNodes
articleTitle: GetChildNodes
second_title: Aspose.Words pour .NET
description: Découvrez la méthode IStructuredDocumentTag GetChildNodes, accédez à une collection dynamique de nœuds enfants adaptés à vos types spécifiés pour une gestion améliorée des documents.
type: docs
weight: 170
url: /fr/net/aspose.words.markup/istructureddocumenttag/getchildnodes/
---
## IStructuredDocumentTag.GetChildNodes method

Renvoie une collection active de nœuds enfants qui correspondent aux types spécifiés.

```csharp
public NodeCollection GetChildNodes(NodeType nodeType, bool isDeep)
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

* class [NodeCollection](../../../aspose.words/nodecollection/)
* enum [NodeType](../../../aspose.words/nodetype/)
* interface [IStructuredDocumentTag](../)
* espace de noms [Aspose.Words.Markup](../../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../../)
