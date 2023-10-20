---
title: NodeList.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words pour .NET
description: NodeList Item propriété. Récupère un nœud à lindex donné en C#.
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

L'indice est de base zéro.

Les index négatifs sont autorisés et indiquent un accès depuis l'arrière de la collection. Par exemple -1 signifie le dernier élément, -2 signifie l'avant-dernier et ainsi de suite.

Si l'index est supérieur ou égal au nombre d'éléments de la liste, cela renvoie une référence nulle.

Si l'index est négatif et que sa valeur absolue est supérieure au nombre d'éléments de la liste, cela renvoie une référence nulle.

## Exemples

Montre comment utiliser XPaths pour parcourir une NodeList.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère quelques nœuds avec un DocumentBuilder.
builder.Writeln("Hello world!");

builder.StartTable();
builder.InsertCell();
builder.Write("Cell 1");
builder.InsertCell();
builder.Write("Cell 2");
builder.EndTable();

#if NET48 || JAVA
builder.InsertImage(Image.FromFile(ImageDir + "Logo.jpg"));
#elif NET5_0_OR_GREATER || __MOBILE__
using (SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg"))
    builder.InsertImage(image);
#endif

// Notre document contient trois nœuds Run.
NodeList nodeList = doc.SelectNodes("//Courir");

Assert.AreEqual(3, nodeList.Count);
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Hello world!"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 1"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 2"));

// Utilisez une double barre oblique pour sélectionner tous les nœuds Run
// qui sont des descendants indirects d'un nœud Table, qui seraient les exécutions à l'intérieur des deux cellules que nous avons insérées.
nodeList = doc.SelectNodes("//Table//Courir");

Assert.AreEqual(2, nodeList.Count);
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 1"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 2"));

// Les barres obliques simples spécifient les relations descendantes directes,
// que nous avons ignoré lorsque nous avons utilisé des doubles barres obliques.
Assert.AreEqual(doc.SelectNodes(" //Table//Exécuter"),
    doc.SelectNodes("//Tableau/Ligne/Cellule/Paragraphe/Exécuter"));

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
