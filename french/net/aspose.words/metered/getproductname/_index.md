---
title: Metered.GetProductName
linktitle: GetProductName
articleTitle: GetProductName
second_title: Aspose.Words pour .NET
description: Découvrez la méthode Metered GetProductName pour récupérer sans effort les noms de produits, améliorant ainsi l'efficacité de votre application et l'expérience utilisateur.
type: docs
weight: 20
url: /fr/net/aspose.words/metered/getproductname/
---
## Metered.GetProductName method

Retourne Nom du produit

```csharp
public string GetProductName()
```

### Return_Value

Nom du produit

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
