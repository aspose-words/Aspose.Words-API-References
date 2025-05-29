---
title: DocumentProperty.ToString
linktitle: ToString
articleTitle: ToString
second_title: Aspose.Words pour .NET
description: Découvrez la méthode DocumentProperty ToString, qui formate les valeurs de propriété sous forme de chaînes en fonction des paramètres régionaux, améliorant ainsi la présentation des données et l'expérience utilisateur.
type: docs
weight: 110
url: /fr/net/aspose.words.properties/documentproperty/tostring/
---
## DocumentProperty.ToString method

Renvoie la valeur de la propriété sous forme de chaîne formatée selon les paramètres régionaux actuels.

```csharp
public override string ToString()
```

## Remarques

Convertit une propriété booléenne en « Y » ou « N ». Convertit une propriété de date en une chaîne de date courte. Pour tous les autres types, convertit une propriété à l'aide de Object.ToString().

## Exemples

Affiche différentes méthodes de conversion de type de propriétés de document personnalisées.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

DateTime authDate = DateTime.Today;
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", authDate);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

Assert.AreEqual(true, properties["Authorized"].ToBool());
Assert.AreEqual("John Doe", properties["Authorized By"].ToString());
Assert.AreEqual(authDate, properties["Authorized Date"].ToDateTime());
Assert.AreEqual(1, properties["Authorized Revision"].ToInt());
Assert.AreEqual(123.45d, properties["Authorized Amount"].ToDouble());
```

Montre comment travailler avec les propriétés de document personnalisées.

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// Chaque document contient une collection de propriétés personnalisées qui, comme les propriétés intégrées, sont des paires clé-valeur.
 // Le document possède une liste fixe de propriétés intégrées. L'utilisateur crée toutes les propriétés personnalisées.
Assert.AreEqual("Value of custom document property", doc.CustomDocumentProperties["CustomProperty"].ToString());

doc.CustomDocumentProperties.Add("CustomProperty2", "Value of custom document property #2");

Console.WriteLine("Custom Properties:");
foreach (var customDocumentProperty in doc.CustomDocumentProperties)
{
    Console.WriteLine(customDocumentProperty.Name);
    Console.WriteLine($"\tType:\t{customDocumentProperty.Type}");
    Console.WriteLine($"\tValue:\t\"{customDocumentProperty.Value}\"");
}
```

### Voir également

* class [DocumentProperty](../)
* espace de noms [Aspose.Words.Properties](../../../aspose.words.properties/)
* Assemblée [Aspose.Words](../../../)
