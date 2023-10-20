---
title: NodeList.ToArray
linktitle: ToArray
articleTitle: ToArray
second_title: Aspose.Words pour .NET
description: NodeList ToArray méthode. Copie tous les nœuds de la collection vers un nouveau tableau de nœuds en C#.
type: docs
weight: 40
url: /fr/net/aspose.words/nodelist/toarray/
---
## NodeList.ToArray method

Copie tous les nœuds de la collection vers un nouveau tableau de nœuds.

```csharp
public Node[] ToArray()
```

### Return_Value

Un tableau de nœuds.

## Remarques

Vous ne devez pas ajouter/supprimer des nœuds lors d'une itération sur une collection de nœuds, car cela invalide l'itérateur et nécessite des actualisations pour les collections en direct.

Pour pouvoir ajouter/supprimer des nœuds pendant l'itération, utilisez cette méthode pour copier les nœuds dans un tableau de taille fixe, puis parcourir le tableau.

## Exemples

Montre comment sélectionner certains nœuds à l’aide d’une expression XPath.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Cette expression extraira tous les nœuds de paragraphe,
// qui sont les descendants de n'importe quel nœud de table du document.
NodeList nodeList = doc.SelectNodes("//Tableau//Paragraphe");

// Parcourez la liste avec un énumérateur et imprimez le contenu de chaque paragraphe dans chaque cellule du tableau.
int index = 0;

using (IEnumerator<Node> e = nodeList.GetEnumerator())
    while (e.MoveNext())
        Console.WriteLine($"Table paragraph index {index++}, contents: \"{e.Current.GetText().Trim()}\"");

// Cette expression sélectionnera tous les paragraphes qui sont des enfants directs de n'importe quel nœud Body du document.
nodeList = doc.SelectNodes("//Corps/Paragraphe");

// On peut traiter la liste comme un tableau.
Assert.AreEqual(4, nodeList.ToArray().Length);

// Utilisez SelectSingleNode pour sélectionner le premier résultat de la même expression que ci-dessus.
Node node = doc.SelectSingleNode("//Corps/Paragraphe");

Assert.AreEqual(typeof(Paragraph), node.GetType());
```

### Voir également

* class [Node](../../node/)
* class [NodeList](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
