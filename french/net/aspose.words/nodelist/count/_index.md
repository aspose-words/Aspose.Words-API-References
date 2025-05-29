---
title: NodeList.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words pour .NET
description: Découvrez la propriété NodeList Count pour récupérer facilement le nombre total de nœuds dans votre liste, améliorant ainsi l'efficacité de votre développement Web.
type: docs
weight: 10
url: /fr/net/aspose.words/nodelist/count/
---
## NodeList.Count property

Obtient le nombre de nœuds dans la liste.

```csharp
public int Count { get; }
```

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

* class [NodeList](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
