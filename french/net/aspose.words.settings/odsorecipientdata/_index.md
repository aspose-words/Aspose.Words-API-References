---
title: OdsoRecipientData Class
linktitle: OdsoRecipientData
articleTitle: OdsoRecipientData
second_title: Aspose.Words pour .NET
description: Aspose.Words.Settings.OdsoRecipientData classe. Représente des informations sur un seul enregistrement dans une source de données externe qui doit être exclu du publipostage en C#.
type: docs
weight: 5930
url: /fr/net/aspose.words.settings/odsorecipientdata/
---
## OdsoRecipientData class

Représente des informations sur un seul enregistrement dans une source de données externe qui doit être exclu du publipostage.

Pour en savoir plus, visitez le[Fusion et publipostage et création de rapports](https://docs.aspose.com/words/net/mail-merge-and-reporting/) article documentaire.

```csharp
public class OdsoRecipientData
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [OdsoRecipientData](odsorecipientdata/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [Active](../../aspose.words.settings/odsorecipientdata/active/) { get; set; } | Spécifie si l'enregistrement de la source de données doit être importé dans un document lors du publipostage. La valeur par défaut est`vrai` . |
| [Column](../../aspose.words.settings/odsorecipientdata/column/) { get; set; } | Spécifie la colonne de la source de données qui contient des données uniques pour l'enregistrement actuel. La valeur par défaut est 0. |
| [Hash](../../aspose.words.settings/odsorecipientdata/hash/) { get; set; } | Représente le code de hachage de cet enregistrement. Parfois, Microsoft Word utilise[`Hash`](./hash/) d'un enregistrement entier au lieu d'un[`UniqueTag`](./uniquetag/) value. La valeur par défaut est 0. |
| [UniqueTag](../../aspose.words.settings/odsorecipientdata/uniquetag/) { get; set; } | Spécifie le contenu d'un enregistrement donné dans la colonne contenant des données uniques. La valeur par défaut est`nul` . |

## Méthodes

| Nom | La description |
| --- | --- |
| [Clone](../../aspose.words.settings/odsorecipientdata/clone/)() | Renvoie un clone profond de cet objet. |

## Remarques

Si un enregistrement doit être fusionné dans un document fusionné, aucune information n’est nécessaire sur cet enregistrement. Cependant, si un enregistrement donné ne doit pas être fusionné dans un document fusionné, alors la valeur de la clé unique pour cet enregistrement doit être stockée dans le[`UniqueTag`](./uniquetag/)propriété de cet objet pour indiquer cette exclusion.

## Exemples

Montre comment accéder à la collection de données qui désigne les enregistrements de source de données de fusion qu'un publipostage exclura.

```csharp
Document doc = new Document(MyDir + "Odso data.docx");

OdsoRecipientDataCollection dataCollection = doc.MailMergeSettings.Odso.RecipientDatas;

Assert.AreEqual(70, dataCollection.Count);

using (IEnumerator<OdsoRecipientData> enumerator = dataCollection.GetEnumerator())
{
    int index = 0;
    while (enumerator.MoveNext())
    {
        Console.WriteLine(
            $"Odso recipient data index {index++} will {(enumerator.Current.Active ? "" : "not ")}be imported upon mail merge.");
        Console.WriteLine($"\tColumn #{enumerator.Current.Column}");
        Console.WriteLine($"\tHash code: {enumerator.Current.Hash}");
        Console.WriteLine($"\tContents array length: {enumerator.Current.UniqueTag.Length}");
    }
}

// Nous pouvons cloner les éléments de cette collection.
Assert.AreNotEqual(dataCollection[0], dataCollection[0].Clone());

// Nous pouvons également supprimer des éléments individuellement ou effacer toute la collection en même temps.
dataCollection.RemoveAt(0);

Assert.AreEqual(69, dataCollection.Count);

dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### Voir également

* espace de noms [Aspose.Words.Settings](../../aspose.words.settings/)
* Assemblée [Aspose.Words](../../)
