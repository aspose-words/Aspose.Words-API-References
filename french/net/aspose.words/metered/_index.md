---
title: Metered Class
linktitle: Metered
articleTitle: Metered
second_title: Aspose.Words pour .NET
description: Aspose.Words.Metered classe. Fournit des méthodes pour définir une clé mesurée en C#.
type: docs
weight: 4160
url: /fr/net/aspose.words/metered/
---
## Metered class

Fournit des méthodes pour définir une clé mesurée.

Pour en savoir plus, visitez le[Licence et abonnement](https://docs.aspose.com/words/net/licensing/) article documentaire.

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
| [SetMeteredKey](../../aspose.words/metered/setmeteredkey/)(*string, string*) | Définit les clés publiques et privées mesurées. Si vous achetez une licence limitée, au démarrage de l'application, cette API doit être appelée, normalement, cela suffit. Cependant, si vous ne parvenez toujours pas à télécharger les données de consommation et dépassez 24 heures, la licence sera définie sur le statut d'évaluation, pour éviter un tel cas, vous devez vérifier régulièrement l'état de la licence, s'il s'agit du statut d'évaluation, appelez à nouveau cette API. |
| static [GetConsumptionCredit](../../aspose.words/metered/getconsumptioncredit/)() | Obtient un crédit de consommation |
| static [GetConsumptionQuantity](../../aspose.words/metered/getconsumptionquantity/)() | Obtient la taille du fichier de consommation |

## Exemples

Dans cet exemple, une tentative sera faite pour définir des clés publiques et privées mesurées

```csharp
[C#]

Metered matered = new Metered();
matered.SetMeteredKey("PublicKey", "PrivateKey");


[Visual Basic]

Dim matered As Metered = New Metered
matered.SetMeteredKey("PublicKey", "PrivateKey")
```

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

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
