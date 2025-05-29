---
title: Metered.GetConsumptionQuantity
linktitle: GetConsumptionQuantity
articleTitle: GetConsumptionQuantity
second_title: Aspose.Words pour .NET
description: Découvrez la méthode GetConsumptionQuantity mesurée pour récupérer efficacement les données de taille de fichier et optimiser la gestion de vos ressources. Améliorez vos analyses de données !
type: docs
weight: 50
url: /fr/net/aspose.words/metered/getconsumptionquantity/
---
## Metered.GetConsumptionQuantity method

Obtient la taille du fichier de consommation

```csharp
public static decimal GetConsumptionQuantity()
```

### Return_Value

quantité de consommation

## Exemples

Montre comment activer une licence mesurée et suivre le crédit/la consommation.

```csharp
// Créez une nouvelle licence mesurée, puis imprimez ses statistiques d'utilisation.
Metered metered = new Metered();
metered.SetMeteredKey("MyPublicKey", "MyPrivateKey");

Console.WriteLine($"Is metered license accepted: {Metered.IsMeteredLicensed()}");
Console.WriteLine($"Product name: {metered.GetProductName()}");
Console.WriteLine($"Credit before operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity before operation: {Metered.GetConsumptionQuantity()}");

// Fonctionnez en utilisant Aspose.Words, puis imprimez à nouveau nos statistiques mesurées pour voir combien nous avons dépensé.
Document doc = new Document(MyDir + "Document.docx");
doc.Save(ArtifactsDir + "Metered.Usage.pdf");

// Le mécanisme de licence mesurée d'Aspose n'envoie pas les données d'utilisation au serveur d'achat à chaque fois,
// vous devez utiliser l'attente.
System.Threading.Thread.Sleep(10000);

Console.WriteLine($"Credit after operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity after operation: {Metered.GetConsumptionQuantity()}");
```

### Voir également

* class [Metered](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
