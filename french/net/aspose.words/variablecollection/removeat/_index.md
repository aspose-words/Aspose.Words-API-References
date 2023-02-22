---
title: VariableCollection.RemoveAt
second_title: Référence de l'API Aspose.Words pour .NET
description: VariableCollection méthode. Supprime une variable de document à lindex spécifié.
type: docs
weight: 90
url: /fr/net/aspose.words/variablecollection/removeat/
---
## VariableCollection.RemoveAt method

Supprime une variable de document à l'index spécifié.

```csharp
public void RemoveAt(int index)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| index | Int32 | L'indice de base zéro. |

### Exemples

Montre comment travailler avec la collection de variables d'un document.

```csharp
Document doc = new Document();
VariableCollection variables = doc.Variables;

// Chaque document a une collection de variables de paires clé/valeur, auxquelles nous pouvons ajouter des éléments.
variables.Add("Home address", "123 Main St.");
variables.Add("City", "London");
variables.Add("Bedrooms", "3");

Assert.AreEqual(3, variables.Count);

// On peut afficher les valeurs des variables dans le corps du document en utilisant les champs DOCVARIABLE.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocVariable field = (FieldDocVariable)builder.InsertField(FieldType.FieldDocVariable, true);
field.VariableName = "Home address";
field.Update();

Assert.AreEqual("123 Main St.", field.Result);

// L'attribution de valeurs aux clés existantes les mettra à jour.
variables.Add("Home address", "456 Queen St.");

// Nous devrons ensuite mettre à jour les champs DOCVARIABLE pour nous assurer qu'ils affichent une valeur à jour.
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

// Énumération sur la collection de variables.
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

// 3 - Efface toute la collection d'un coup :
variables.Clear();

Assert.That(variables, Is.Empty);
```

### Voir également

* class [VariableCollection](../)
* espace de noms [Aspose.Words](../../variablecollection/)
* Assemblée [Aspose.Words](../../../)


