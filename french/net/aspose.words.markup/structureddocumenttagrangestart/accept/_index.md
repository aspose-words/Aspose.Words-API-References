---
title: StructuredDocumentTagRangeStart.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words pour .NET
description: Découvrez comment la méthode StructuredDocumentTagRangeStart Accept améliore le traitement des documents en acceptant efficacement les visiteurs pour une intégration transparente.
type: docs
weight: 200
url: /fr/net/aspose.words.markup/structureddocumenttagrangestart/accept/
---
## StructuredDocumentTagRangeStart.Accept method

Accepte un visiteur.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| visitor | DocumentVisitor | Le visiteur qui visitera les nœuds. |

### Return_Value

Vrai si tous les nœuds ont été visités ; faux si[`DocumentVisitor`](../../../aspose.words/documentvisitor/) a arrêté l'opération avant de visiter tous les nœuds.

## Remarques

Énumère ce nœud et tous ses enfants. Chaque nœud appelle une méthode correspondante sur[`DocumentVisitor`](../../../aspose.words/documentvisitor/).

Pour plus d'informations, consultez le modèle de conception Visitor.

### Voir également

* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [StructuredDocumentTagRangeStart](../)
* espace de noms [Aspose.Words.Markup](../../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../../)
