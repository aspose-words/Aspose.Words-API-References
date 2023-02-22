---
title: OdsoRecipientDataCollection.RemoveAt
second_title: Référence de l'API Aspose.Words pour .NET
description: OdsoRecipientDataCollection méthode. Supprime lélément à lindex spécifié.
type: docs
weight: 70
url: /fr/net/aspose.words.settings/odsorecipientdatacollection/removeat/
---
## OdsoRecipientDataCollection.RemoveAt method

Supprime l'élément à l'index spécifié.

```csharp
public void RemoveAt(int index)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| index | Int32 | Index de base zéro de l'élément. |

### Exemples

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

// Nous pouvons également supprimer des éléments individuellement ou effacer toute la collection en une seule fois.
dataCollection.RemoveAt(0);

Assert.AreEqual(69, dataCollection.Count);

dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### Voir également

* class [OdsoRecipientDataCollection](../)
* espace de noms [Aspose.Words.Settings](../../odsorecipientdatacollection/)
* Assemblée [Aspose.Words](../../../)


