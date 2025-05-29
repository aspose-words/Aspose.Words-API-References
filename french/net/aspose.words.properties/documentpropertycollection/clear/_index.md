---
title: DocumentPropertyCollection.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words pour .NET
description: Supprimez facilement toutes les propriétés de votre DocumentPropertyCollection grâce à notre méthode Clear. Simplifiez la gestion de vos données dès aujourd'hui !
type: docs
weight: 30
url: /fr/net/aspose.words.properties/documentpropertycollection/clear/
---
## DocumentPropertyCollection.Clear method

Supprime toutes les propriétés de la collection.

```csharp
public void Clear()
```

## Exemples

Montre comment travailler avec les propriétés personnalisées d'un document.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

// Les propriétés de document personnalisées sont des paires clé-valeur que nous pouvons ajouter au document.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// La collection trie les propriétés personnalisées par ordre alphabétique.
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

// Imprimez chaque propriété personnalisée dans le document.
using (IEnumerator<DocumentProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: \"{enumerator.Current.Name}\"\n\tType: \"{enumerator.Current.Type}\"\n\tValue: \"{enumerator.Current.Value}\"");
}

// Affichez la valeur d'une propriété personnalisée à l'aide d'un champ DOCPROPERTY.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.AreEqual("John Doe", field.Result);

// Nous pouvons trouver ces propriétés personnalisées dans Microsoft Word via "Fichier" -> "Propriétés" -> "Propriétés avancées" -> "Personnalisé".
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// Vous trouverez ci-dessous trois manières de supprimer les propriétés personnalisées d'un document.
// 1 - Supprimer par index :
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - Supprimer par nom :
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - Vider toute la collection en une seule fois :
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### Voir également

* class [DocumentPropertyCollection](../)
* espace de noms [Aspose.Words.Properties](../../../aspose.words.properties/)
* Assemblée [Aspose.Words](../../../)
