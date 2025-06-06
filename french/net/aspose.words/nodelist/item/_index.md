---
title: NodeList.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words pour .NET
description: Accédez facilement à des nœuds spécifiques grâce à la propriété NodeList Item. Récupérez les nœuds par index pour une manipulation simplifiée des données et un codage efficace.
type: docs
weight: 20
url: /fr/net/aspose.words/nodelist/item/
---
## NodeList indexer

Récupère un nœud à l'index donné.

```csharp
public Node this[int index] { get; }
```

| Paramètre | La description |
| --- | --- |
| index | Un index dans la liste des nœuds. |

## Remarques

L'indice est basé sur zéro.

Les index négatifs sont autorisés et indiquent l'accès depuis l'arrière de la collection. Par exemple, -1 signifie le dernier élément, -2 signifie l'avant-dernier et ainsi de suite.

Si l'index est supérieur ou égal au nombre d'éléments dans la liste, cela renvoie une référence nulle.

Si l'index est négatif et que sa valeur absolue est supérieure au nombre d'éléments dans la liste, cela renvoie une référence nulle.

## Exemples

Montre comment utiliser XPaths pour naviguer dans une NodeList.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer quelques nœuds avec un DocumentBuilder.
builder.Writeln("Hello world!");

builder.StartTable();
builder.InsertCell();
builder.Write("Cell 1");
builder.InsertCell();
builder.Write("Cell 2");
builder.EndTable();

builder.InsertImage(ImageDir + "Logo.jpg");

// Notre document contient trois nœuds Run.
NodeList nodeList = doc.SelectNodes("//Courir");

Assert.AreEqual(3, nodeList.Count);
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Hello world!"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 1"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 2"));

// Utilisez une double barre oblique pour sélectionner tous les nœuds d'exécution
// qui sont des descendants indirects d'un nœud de table, qui seraient les exécutions à l'intérieur des deux cellules que nous avons insérées.
nodeList = doc.SelectNodes("//Table//Courir");

Assert.AreEqual(2, nodeList.Count);
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 1"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 2"));

// Les barres obliques simples spécifient les relations descendantes directes,
// que nous avons ignoré lorsque nous avons utilisé des doubles barres obliques.
Assert.AreEqual(doc.SelectNodes(" //Table//Exécuter"),
    doc.SelectNodes("//Tableau/Ligne/Cellule/Paragraphe/Exécution"));

// Accédez à la forme qui contient l'image que nous avons insérée.
nodeList = doc.SelectNodes("//Forme");

Assert.AreEqual(1, nodeList.Count);

Shape shape = (Shape)nodeList[0];
Assert.True(shape.HasImage);
```

### Voir également

* class [Node](../../node/)
* class [NodeList](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
