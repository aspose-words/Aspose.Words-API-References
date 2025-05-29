---
title: CompositeNode.HasChildNodes
linktitle: HasChildNodes
articleTitle: HasChildNodes
second_title: Aspose.Words pour .NET
description: Découvrez si un CompositeNode possède des nœuds enfants grâce à la propriété HasChildNodes. Simplifiez votre codage grâce à cette fonctionnalité essentielle pour une gestion efficace des nœuds.
type: docs
weight: 30
url: /fr/net/aspose.words/compositenode/haschildnodes/
---
## CompositeNode.HasChildNodes property

Retours`vrai` si ce nœud a des nœuds enfants.

```csharp
public bool HasChildNodes { get; }
```

## Exemples

Montre comment combiner les lignes de deux tables en une seule.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Vous trouverez ci-dessous deux manières d’obtenir un tableau à partir d’un document.
// 1 - À partir de la collection « Tables » d'un nœud Body :
Table firstTable = doc.FirstSection.Body.Tables[0];

// 2 - Utilisation de la méthode « GetChild » :
Table secondTable = (Table)doc.GetChild(NodeType.Table, 1, true);

// Ajouter toutes les lignes de la table actuelle à la suivante.
while (secondTable.HasChildNodes)
    firstTable.Rows.Add(secondTable.FirstRow);

// Supprimez le conteneur de table vide.
secondTable.Remove();

doc.Save(ArtifactsDir + "Table.CombineTables.docx");
```

### Voir également

* class [CompositeNode](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
