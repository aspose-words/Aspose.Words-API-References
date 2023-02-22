---
title: DocumentProperty.ToDouble
second_title: Référence de l'API Aspose.Words pour .NET
description: DocumentProperty méthode. Renvoie la valeur de la propriété sous la forme double.
type: docs
weight: 90
url: /fr/net/aspose.words.properties/documentproperty/todouble/
---
## DocumentProperty.ToDouble method

Renvoie la valeur de la propriété sous la forme double.

```csharp
public double ToDouble()
```

### Remarques

Lève une exception si le type de propriété n'est pasNumber .

### Exemples

Affiche diverses méthodes de conversion de type des propriétés de document personnalisées.

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

### Voir également

* class [DocumentProperty](../)
* espace de noms [Aspose.Words.Properties](../../documentproperty/)
* Assemblée [Aspose.Words](../../../)


