---
title: VariableCollection.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words pour .NET
description: Supprimez facilement les variables de document grâce à la méthode VariableCollection Remove. Simplifiez la gestion de vos données grâce à cette solution efficace.
type: docs
weight: 80
url: /fr/net/aspose.words/variablecollection/remove/
---
## VariableCollection.Remove method

Supprime une variable de document portant le nom spécifié de la collection.

```csharp
public void Remove(string name)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| name | String | Le nom de la variable, insensible à la casse. |

## Exemples

Montre comment travailler avec la collection de variables d'un document.

```csharp
Document doc = new Document();
VariableCollection variables = doc.Variables;

// Chaque document possède une collection de variables de paires clé/valeur, auxquelles nous pouvons ajouter des éléments.
variables.Add("Home address", "123 Main St.");
variables.Add("City", "London");
variables.Add("Bedrooms", "3");

Assert.AreEqual(3, variables.Count);

// Nous pouvons afficher les valeurs des variables dans le corps du document en utilisant les champs DOCVARIABLE.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocVariable field = (FieldDocVariable)builder.InsertField(FieldType.FieldDocVariable, true);
field.VariableName = "Home address";
field.Update();

Assert.AreEqual("123 Main St.", field.Result);

// L'attribution de valeurs aux clés existantes les mettra à jour.
variables.Add("Home address", "456 Queen St.");

// Nous devrons ensuite mettre à jour les champs DOCVARIABLE pour garantir qu'ils affichent une valeur à jour.
Assert.AreEqual("123 Main St.", field.Result);

field.Update();

Assert.AreEqual("456 Queen St.", field.Result);

// Vérifiez que les variables de document avec un certain nom ou une certaine valeur existent.
Assert.True(variables.Contains("City"));
Assert.True(variables.Any(v => v.Value == "London"));

// La collection de variables trie automatiquement les variables par ordre alphabétique de nom.
Assert.AreEqual(0, variables.IndexOfKey("Bedrooms"));
Assert.AreEqual(1, variables.IndexOfKey("City"));
Assert.AreEqual(2, variables.IndexOfKey("Home address"));

Assert.AreEqual("3", variables[0]);
Assert.AreEqual("London", variables["City"]);

// Énumérer sur la collection de variables.
using (IEnumerator<KeyValuePair<string, string>> enumerator = doc.Variables.GetEnumerator())
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: {enumerator.Current.Key}, Value: {enumerator.Current.Value}");

// Vous trouverez ci-dessous trois manières de supprimer des variables de document d'une collection.
// 1 - Par nom :
variables.Remove("City");

Assert.False(variables.Contains("City"));

// 2 - Par index :
variables.RemoveAt(1);

Assert.False(variables.Contains("Home address"));

// 3 - Effacer toute la collection en une seule fois :
variables.Clear();

Assert.AreEqual(0, variables.Count);
```

### Voir également

* class [VariableCollection](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
