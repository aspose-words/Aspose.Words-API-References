---
title: PropertyType Enum
linktitle: PropertyType
articleTitle: PropertyType
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.PropertyType pour définir facilement les types de données de propriétés de document pour une gestion et une personnalisation améliorées des documents.
type: docs
weight: 5230
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
| DateTime | `1` | La propriété est une valeur de date et d'heure. |
| Double | `2` | La propriété est un nombre flottant. |
| Number | `3` | La propriété est un nombre entier. |
| String | `4` | La propriété est une valeur de chaîne. |
| StringArray | `5` | La propriété est un tableau de chaînes. |
| ObjectArray | `6` | La propriété est un tableau d'objets. |
| ByteArray | `7` | La propriété est un tableau d'octets. |
| Other | `8` | La propriété est d'un autre type. |

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

* class [DocumentProperty](../documentproperty/)
* property [Type](../documentproperty/type/)
* espace de noms [Aspose.Words.Properties](../../aspose.words.properties/)
* Assemblée [Aspose.Words](../../)
