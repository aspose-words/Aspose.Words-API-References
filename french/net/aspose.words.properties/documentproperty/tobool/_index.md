---
title: DocumentProperty.ToBool
linktitle: ToBool
articleTitle: ToBool
second_title: Aspose.Words pour .NET
description: Découvrez la méthode DocumentProperty ToBool qui convertit efficacement les valeurs de propriété en valeurs booléennes pour une gestion transparente des données et une efficacité de codage améliorée.
type: docs
weight: 60
url: /fr/net/aspose.words.properties/documentproperty/tobool/
---
## DocumentProperty.ToBool method

Renvoie la valeur de la propriété sous forme booléenne.

```csharp
public bool ToBool()
```

## Remarques

Lève une exception si le type de propriété n'est pasBoolean.

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
