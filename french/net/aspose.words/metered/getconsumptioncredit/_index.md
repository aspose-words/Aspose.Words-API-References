---
title: Metered.GetConsumptionCredit
second_title: Référence de l'API Aspose.Words pour .NET
description: Metered méthode. Obtient un crédit de consommation
type: docs
weight: 30
url: /fr/net/aspose.words/metered/getconsumptioncredit/
---
## Metered.GetConsumptionCredit method

Obtient un crédit de consommation

```csharp
public static decimal GetConsumptionCredit()
```

### Return_Value

quantité consommée

### Exemples

Montre comment activer une licence au compteur et suivre le crédit/la consommation.

```csharp
// Créez une nouvelle licence avec compteur, puis imprimez ses statistiques d'utilisation.
Metered metered = new Metered();
metered.SetMeteredKey("MyPublicKey", "MyPrivateKey");

Console.WriteLine($"Credit before operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity before operation: {Metered.GetConsumptionQuantity()}");

// Opérez en utilisant Aspose.Words, puis imprimez à nouveau nos statistiques mesurées pour voir combien nous avons dépensé.
Document doc = new Document(MyDir + "Document.docx");
doc.Save(ArtifactsDir + "Metered.Usage.pdf");

// Le mécanisme Aspose Metered Licensing n'envoie pas les données d'utilisation au serveur d'achat à chaque fois,
// vous devez utiliser l'attente.
System.Threading.Thread.Sleep(10000);

Console.WriteLine($"Credit after operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity after operation: {Metered.GetConsumptionQuantity()}");
```

### Voir également

* class [Metered](../)
* espace de noms [Aspose.Words](../../metered/)
* Assemblée [Aspose.Words](../../../)


