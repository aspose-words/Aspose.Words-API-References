---
title: PropertyType Enum
linktitle: PropertyType
articleTitle: PropertyType
second_title: Aspose.Words pour .NET
description: Aspose.Words.Properties.PropertyType énumération. Spécifie le type de données dune propriété de document en C#.
type: docs
weight: 4500
url: /fr/net/aspose.words.properties/propertytype/
---
## PropertyType enumeration

Spécifie le type de données d'une propriété de document.

```csharp
public enum PropertyType
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Boolean | `0` | La propriété est une valeur booléenne. |
| DateTime | `1` | La propriété est une valeur date/heure. |
| Double | `2` | La propriété est un nombre flottant. |
| Number | `3` | La propriété est un nombre entier. |
| String | `4` | La propriété est une valeur de chaîne. |
| StringArray | `5` | La propriété est un tableau de chaînes. |
| ObjectArray | `6` | La propriété est un tableau d'objets. |
| ByteArray | `7` | La propriété est un tableau d'octets. |
| Other | `8` | La propriété est d'un autre type. |

## Exemples

Montre comment utiliser les propriétés personnalisées d'un document.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

// Les propriétés du document personnalisé sont des paires clé-valeur que nous pouvons ajouter au document.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// La collection trie les propriétés personnalisées par ordre alphabétique.
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

// Imprime chaque propriété personnalisée du document.
using (IEnumerator<DocumentProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: \"{enumerator.Current.Name}\"\n\tType: \"{enumerator.Current.Type}\"\n\tValue: \"{enumerator.Current.Value}\"");
}

// Affiche la valeur d'une propriété personnalisée à l'aide d'un champ DOCPROPERTY.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.AreEqual("John Doe", field.Result);

// Nous pouvons retrouver ces propriétés personnalisées dans Microsoft Word via "Fichier" -> "Propriétés" > "Propriétés avancées" > "Coutume".
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// Vous trouverez ci-dessous trois manières de supprimer les propriétés personnalisées d'un document.
// 1 - Supprimer par index :
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - Supprimer par nom :
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - Vider toute la collection d'un coup :
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### Voir également

* class [DocumentProperty](../documentproperty/)
* property [Type](../documentproperty/type/)
* espace de noms [Aspose.Words.Properties](../../aspose.words.properties/)
* Assemblée [Aspose.Words](../../)
