---
title: Metered.SetMeteredKey
linktitle: SetMeteredKey
articleTitle: SetMeteredKey
second_title: Aspose.Words pour .NET
description: Gérez facilement votre licence mesurée grâce à la méthode SetMeteredKey. Assurez des téléchargements de données fluides et évitez les évaluations grâce à des contrôles réguliers.
type: docs
weight: 30
url: /fr/net/aspose.words/metered/setmeteredkey/
---
## Metered.SetMeteredKey method

Définit les clés publiques et privées mesurées. Si vous achetez une licence mesurée, au démarrage de l'application, cette API doit être appelée, normalement, cela suffit. Cependant, si le téléchargement des données de consommation échoue systématiquement et dépasse 24 heures, la licence sera définie sur le statut d'évaluation. Pour éviter ce problème, vous devez vérifier régulièrement le statut de la licence. Si c'est le statut d'évaluation, appelez à nouveau cette API.

```csharp
public void SetMeteredKey(string publicKey, string privateKey)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| publicKey | String | clé publique |
| privateKey | String | clé privée |

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
