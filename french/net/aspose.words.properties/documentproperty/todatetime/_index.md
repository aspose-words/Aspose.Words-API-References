---
title: DocumentProperty.ToDateTime
linktitle: ToDateTime
articleTitle: ToDateTime
second_title: Aspose.Words pour .NET
description: Convertissez facilement DocumentProperty en DateTime UTC. Accédez à des horodatages précis et optimisez la gestion de vos données grâce à notre méthode fiable.
type: docs
weight: 80
url: /fr/net/aspose.words.properties/documentproperty/todatetime/
---
## DocumentProperty.ToDateTime method

Renvoie la valeur de la propriété sous la forme**Date et heure** en UTC.

```csharp
public DateTime ToDateTime()
```

## Remarques

Lève une exception si le type de propriété n'est pasDateTime.

Microsoft Word stocke uniquement la partie date (pas l'heure) pour les propriétés de date personnalisées.

## Exemples

Montre comment créer une propriété de document personnalisée contenant une date et une heure.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("AuthorizationDate", DateTime.Now);
DateTime authorizationDate = doc.CustomDocumentProperties["AuthorizationDate"].ToDateTime();
Console.WriteLine($"Document authorized on {authorizationDate}");
```

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
