---
title: NodeCollection.Insert
linktitle: Insert
articleTitle: Insert
second_title: Aspose.Words pour .NET
description: Insérez facilement des nœuds dans votre NodeCollection à n'importe quel index grâce à notre méthode d'insertion simplifiée. Optimisez la gestion de vos données dès aujourd'hui !
type: docs
weight: 80
url: /fr/net/aspose.words/nodecollection/insert/
---
## NodeCollection.Insert method

Insère un nœud dans la collection à l'index spécifié.

```csharp
public void Insert(int index, Node node)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| index | Int32 | L'index de base zéro du nœud. Les index négatifs sont autorisés et indiquent l'accès depuis l'arrière de la liste. Par exemple, -1 signifie le dernier nœud, -2 signifie l'avant-dernier et ainsi de suite. |
| node | Node | Le nœud à insérer. |

### Exceptions

| exception | condition |
| --- | --- |
| NotSupportedException | Le[`NodeCollection`](../) est une collection « profonde ». |

## Remarques

Le nœud est inséré en tant qu’enfant dans l’objet nœud à partir duquel la collection a été créée.

Si l'indice est égal ou supérieur à[`Count`](../count/), le nœud est ajouté à la fin de la collection.

Si l'indice est négatif et sa valeur absolue est supérieure à[`Count`](../count/), le nœud est ajouté à la fin de la collection.

Si le nœud inséré a été créé à partir d'un autre document, vous devez utiliser [`ImportNode`](../../documentbase/importnode/) pour importer le nœud dans le document actuel. Le nœud importé peut ensuite être inséré dans le document actuel.

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
