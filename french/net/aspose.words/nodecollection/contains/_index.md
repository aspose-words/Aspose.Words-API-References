---
title: NodeCollection.Contains
linktitle: Contains
articleTitle: Contains
second_title: Aspose.Words pour .NET
description: Découvrez comment la méthode NodeCollection Contains vérifie efficacement si un nœud existe dans votre collection, améliorant ainsi vos capacités de gestion des données.
type: docs
weight: 50
url: /fr/net/aspose.words/nodecollection/contains/
---
## NodeCollection.Contains method

Détermine si un nœud est dans la collection.

```csharp
public bool Contains(Node node)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| node | Node | Le nœud à localiser. |

### Return_Value

`vrai`si l'élément est trouvé dans la collection ; sinon,`FAUX`.

## Remarques

Cette méthode effectue une recherche linéaire ; par conséquent, le temps d'exécution moyen est proportionnel à[`Count`](../count/).

## Exemples

Montre comment travailler avec une NodeCollection.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ajoutez du texte au document en insérant des exécutions à l'aide d'un DocumentBuilder.
builder.Write("Run 1. ");
builder.Write("Run 2. ");

// Chaque invocation de la méthode « Write » crée une nouvelle exécution,
// qui apparaît ensuite dans la RunCollection du paragraphe parent.
RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;

Assert.AreEqual(2, runs.Count);

// Nous pouvons également insérer un nœud dans RunCollection manuellement.
Run newRun = new Run(doc, "Run 3. ");
runs.Insert(3, newRun);

Assert.True(runs.Contains(newRun));
Assert.AreEqual("Run 1. Run 2. Run 3.", doc.GetText().Trim());

// Accédez aux exécutions individuelles et supprimez-les pour supprimer leur texte du document.
Run run = runs[1];
runs.Remove(run);

Assert.AreEqual("Run 1. Run 3.", doc.GetText().Trim());
Assert.NotNull(run);
Assert.False(runs.Contains(run));
```

### Voir également

* class [Node](../../node/)
* class [NodeCollection](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
