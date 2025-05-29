---
title: XmlMapping.StoreItemId
linktitle: StoreItemId
articleTitle: StoreItemId
second_title: Aspose.Words pour .NET
description: Découvrez la propriété XmlMapping StoreItemId pour les identifiants de données XML personnalisés. Améliorez l'évaluation XPath grâce à nos solutions uniques pour une gestion efficace des données.
type: docs
weight: 40
url: /fr/net/aspose.words.markup/xmlmapping/storeitemid/
---
## XmlMapping.StoreItemId property

Spécifie l'identifiant de données XML personnalisé pour la partie de données XML personnalisée qui doit être utilisé pour évaluer le[`XPath`](../xpath/) expression.

```csharp
public string StoreItemId { get; }
```

## Exemples

Montre comment obtenir l'identifiant de données XML personnalisé d'une partie XML.

```csharp
Document doc = new Document(MyDir + "Custom XML part in structured document tag.docx");

// Les balises de documents structurés ont des identifiants sous la forme de GUID.
StructuredDocumentTag tag = (StructuredDocumentTag)doc.GetChild(NodeType.StructuredDocumentTag, 0, true);

Assert.AreEqual("{F3029283-4FF8-4DD2-9F31-395F19ACEE85}", tag.XmlMapping.StoreItemId);
```

### Voir également

* class [XmlMapping](../)
* espace de noms [Aspose.Words.Markup](../../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../../)
