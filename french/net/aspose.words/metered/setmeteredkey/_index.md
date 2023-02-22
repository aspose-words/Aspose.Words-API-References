---
title: Metered.SetMeteredKey
second_title: Référence de l'API Aspose.Words pour .NET
description: Metered méthode. Définit la clé publique et privée mesurée. Si vous achetez une licence mesurée lorsque vous démarrez lapplication cette API doit être appelée normalement cela suffit. Cependant si vous ne parvenez toujours pas à télécharger les données de consommation et dépassez 24 heures la licence sera définie sur le statut dévaluation pour éviter ce cas vous devez vérifier régulièrement le statut de la licence sil sagit du statut dévaluation appelez à nouveau cette API.
type: docs
weight: 20
url: /fr/net/aspose.words/metered/setmeteredkey/
---
## Metered.SetMeteredKey method

Définit la clé publique et privée mesurée. Si vous achetez une licence mesurée, lorsque vous démarrez l'application, cette API doit être appelée, normalement, cela suffit. Cependant, si vous ne parvenez toujours pas à télécharger les données de consommation et dépassez 24 heures, la licence sera définie sur le statut d'évaluation, pour éviter ce cas, vous devez vérifier régulièrement le statut de la licence, s'il s'agit du statut d'évaluation, appelez à nouveau cette API.

```csharp
public void SetMeteredKey(string publicKey, string privateKey)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| publicKey | String | Clé publique |
| privateKey | String | Clé privée |

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


