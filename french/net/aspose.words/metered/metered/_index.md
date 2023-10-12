---
title: Metered.Metered
second_title: Référence de l'API Aspose.Words pour .NET
description: Metered constructeur. Initialise une nouvelle instance de cette classe.
type: docs
weight: 10
url: /fr/net/aspose.words/metered/metered/
---
## Metered constructor

Initialise une nouvelle instance de cette classe.

```csharp
public Metered()
```

### Exemples

Montre comment activer une licence avec compteur et suivre le crédit/la consommation.

```csharp
// Créez une nouvelle licence limitée, puis imprimez ses statistiques d'utilisation.
Metered metered = new Metered();
metered.SetMeteredKey("MyPublicKey", "MyPrivateKey");

Console.WriteLine($"Credit before operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity before operation: {Metered.GetConsumptionQuantity()}");

// Fonctionne en utilisant Aspose.Words, puis imprime à nouveau nos statistiques mesurées pour voir combien nous avons dépensé.
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


