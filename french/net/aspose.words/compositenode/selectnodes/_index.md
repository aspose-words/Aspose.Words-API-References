---
title: CompositeNode.SelectNodes
linktitle: SelectNodes
articleTitle: SelectNodes
second_title: Aspose.Words pour .NET
description: Récupérez sans effort des nœuds avec la méthode CompositeNode SelectNodes à l'aide d'expressions XPath pour une manipulation améliorée des données et un codage simplifié.
type: docs
weight: 210
url: /fr/net/aspose.words/compositenode/selectnodes/
---
## CompositeNode.SelectNodes method

Sélectionne une liste de nœuds correspondant à l'expression XPath.

```csharp
public NodeList SelectNodes(string xpath)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| xpath | String | L'expression XPath. |

### Return_Value

Une liste de nœuds correspondant à la requête XPath.

## Remarques

Seules les expressions avec des noms d'éléments sont actuellement prises en charge. Les expressions utilisant des noms d'attributs ne sont pas prises en charge.

## Exemples

Montre comment utiliser une expression XPath pour tester si un nœud se trouve à l'intérieur d'un champ.

```csharp
Document doc = new Document(MyDir + "Mail merge destination - Northwind employees.docx");

// La NodeList qui résulte de cette expression XPath contiendra tous les nœuds que nous trouvons à l'intérieur d'un champ.
// Cependant, les nœuds FieldStart et FieldEnd peuvent figurer sur la liste s'il existe des champs imbriqués dans le chemin.
// Actuellement, ne trouve pas de champs rares dans lesquels le FieldCode ou le FieldResult s'étend sur plusieurs paragraphes.
NodeList resultList =
    doc.SelectNodes("//FieldStart/following-sibling::node()[following-sibling::FieldEnd]");

// Vérifiez si l'exécution spécifiée est l'un des nœuds qui se trouvent à l'intérieur du champ.
Console.WriteLine($"Contents of the first Run node that's part of a field: {resultList.First(n => n.NodeType == NodeType.Run).GetText().Trim()}");
```

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

* class [NodeList](../../nodelist/)
* class [CompositeNode](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
