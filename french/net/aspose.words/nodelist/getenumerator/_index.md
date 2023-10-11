---
title: NodeList.GetEnumerator
second_title: Référence de l'API Aspose.Words pour .NET
description: NodeList méthode. Fournit une simple itération de style foreach sur la collection de nœuds.
type: docs
weight: 30
url: /fr/net/aspose.words/nodelist/getenumerator/
---
## NodeList.GetEnumerator method

Fournit une simple itération de style "foreach" sur la collection de nœuds.

```csharp
public IEnumerator<Node> GetEnumerator()
```

### Return_Value

Un IEnumérateur.

### Exemples

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
* espace de noms [Aspose.Words](../../nodelist/)
* Assemblée [Aspose.Words](../../../)


