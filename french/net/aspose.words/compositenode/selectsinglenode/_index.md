---
title: CompositeNode.SelectSingleNode
linktitle: SelectSingleNode
articleTitle: SelectSingleNode
second_title: Aspose.Words pour .NET
description: Découvrez comment la méthode SelectSingleNode de CompositeNode récupère efficacement le premier nœud correspondant à votre expression XPath pour une gestion simplifiée des données.
type: docs
weight: 220
url: /fr/net/aspose.words/compositenode/selectsinglenode/
---
## CompositeNode.SelectSingleNode method

Sélectionne le premier[`Node`](../../node/) qui correspond à l'expression XPath.

```csharp
public Node SelectSingleNode(string xpath)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| xpath | String | L'expression XPath. |

### Return_Value

Le premier[`Node`](../../node/) qui correspond à la requête XPath ou`nul` si aucun nœud correspondant n'est trouvé.

## Remarques

Seules les expressions avec des noms d'éléments sont actuellement prises en charge. Les expressions utilisant des noms d'attributs ne sont pas prises en charge.

## Exemples

Montre comment sélectionner certains nœuds à l’aide d’une expression XPath.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Cette expression extraira tous les nœuds de paragraphe,
// qui sont les descendants de n'importe quel nœud de table dans le document.
NodeList nodeList = doc.SelectNodes("//Tableau//Paragraphe");

// Parcourez la liste avec un énumérateur et imprimez le contenu de chaque paragraphe dans chaque cellule du tableau.
int index = 0;

using (IEnumerator<Node> e = nodeList.GetEnumerator())
    while (e.MoveNext())
        Console.WriteLine($"Table paragraph index {index++}, contents: \"{e.Current.GetText().Trim()}\"");

// Cette expression sélectionnera tous les paragraphes qui sont des enfants directs de n'importe quel nœud Corps dans le document.
nodeList = doc.SelectNodes("//Corps/Paragraphe");

// Nous pouvons traiter la liste comme un tableau.
Assert.AreEqual(4, nodeList.ToArray().Length);

// Utilisez SelectSingleNode pour sélectionner le premier résultat de la même expression que ci-dessus.
Node node = doc.SelectSingleNode("//Corps/Paragraphe");

Assert.AreEqual(typeof(Paragraph), node.GetType());
```

### Voir également

* class [Node](../../node/)
* class [CompositeNode](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
