---
title: DocumentProperty.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words pour .NET
description: Découvrez le type DocumentProperty pour récupérer et utiliser efficacement les types de données de propriété pour une gestion et une automatisation améliorées des documents.
type: docs
weight: 40
url: /fr/net/aspose.words.properties/documentproperty/type/
---
## DocumentProperty.Type property

Obtient le type de données de la propriété.

```csharp
public PropertyType Type { get; }
```

## Exemples

Montre comment travailler avec les propriétés de document intégrées.

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// L'objet « Document » contient certaines de ses métadonnées dans ses membres.
Console.WriteLine($"Document filename:\n\t \"{doc.OriginalFileName}\"");

// Le document stocke également des métadonnées dans ses propriétés intégrées.
// Chaque propriété intégrée est un membre de l'objet « BuiltInDocumentProperties » du document.
Console.WriteLine("Built-in Properties:");
foreach (DocumentProperty docProperty in doc.BuiltInDocumentProperties)
{
    Console.WriteLine(docProperty.Name);
    Console.WriteLine($"\tType:\t{docProperty.Type}");

    // Certaines propriétés peuvent stocker plusieurs valeurs.
    if (docProperty.Value is ICollection<object>)
    {
        foreach (object value in docProperty.Value as ICollection<object>)
            Console.WriteLine($"\tValue:\t\"{value}\"");
    }
    else
    {
        Console.WriteLine($"\tValue:\t\"{docProperty.Value}\"");
    }
}
```

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

* enum [PropertyType](../../propertytype/)
* class [DocumentProperty](../)
* espace de noms [Aspose.Words.Properties](../../../aspose.words.properties/)
* Assemblée [Aspose.Words](../../../)
