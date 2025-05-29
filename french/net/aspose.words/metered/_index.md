---
title: Metered Class
linktitle: Metered
articleTitle: Metered
second_title: Aspose.Words pour .NET
description: Exploitez la puissance de la classe Aspose.Words.Metered ! Gérez facilement votre clé mesurée grâce à des méthodes efficaces pour un traitement fluide des documents.
type: docs
weight: 4850
url: /fr/net/aspose.words/metered/
---
## Metered class

Fournit des méthodes pour définir la clé mesurée.

```csharp
public class Metered
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [Metered](metered/)() | Initialise une nouvelle instance de cette classe. |

## Méthodes

| Nom | La description |
| --- | --- |
| [GetProductName](../../aspose.words/metered/getproductname/)() | Retourne Nom du produit |
| [SetMeteredKey](../../aspose.words/metered/setmeteredkey/)(*string, string*) | Définit les clés publiques et privées mesurées. Si vous achetez une licence mesurée, au démarrage de l'application, cette API doit être appelée, normalement, cela suffit. Cependant, si le téléchargement des données de consommation échoue systématiquement et dépasse 24 heures, la licence sera définie sur le statut d'évaluation. Pour éviter ce problème, vous devez vérifier régulièrement le statut de la licence. Si c'est le statut d'évaluation, appelez à nouveau cette API. |
| static [GetConsumptionCredit](../../aspose.words/metered/getconsumptioncredit/)() | Obtient un crédit de consommation |
| static [GetConsumptionQuantity](../../aspose.words/metered/getconsumptionquantity/)() | Obtient la taille du fichier de consommation |
| static [IsMeteredLicensed](../../aspose.words/metered/ismeteredlicensed/)() | Vérifiez si le compteur est sous licence |

## Exemples

Dans cet exemple, une tentative sera faite pour définir une clé publique et privée mesurée

```csharp
[C#]

Metered matered = new Metered();
matered.SetMeteredKey("PublicKey", "PrivateKey");


[Visual Basic]

Dim matered As Metered = New Metered
matered.SetMeteredKey("PublicKey", "PrivateKey")
```

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

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
