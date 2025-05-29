---
title: DocumentProperty.ToDouble
linktitle: ToDouble
articleTitle: ToDouble
second_title: Aspose.Words pour .NET
description: Convertissez facilement les valeurs DocumentProperty en valeurs doubles grâce à la méthode ToDouble. Bénéficiez dès aujourd'hui d'une gestion précise des données pour vos applications !
type: docs
weight: 90
url: /fr/net/aspose.words.properties/documentproperty/todouble/
---
## DocumentProperty.ToDouble method

Renvoie la valeur de la propriété sous forme de double.

```csharp
public double ToDouble()
```

## Remarques

Lève une exception si le type de propriété n'est pasNumber .

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

### Voir également

* class [DocumentProperty](../)
* espace de noms [Aspose.Words.Properties](../../../aspose.words.properties/)
* Assemblée [Aspose.Words](../../../)
