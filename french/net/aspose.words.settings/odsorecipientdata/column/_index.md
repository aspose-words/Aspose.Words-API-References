---
title: OdsoRecipientData.Column
second_title: Référence de l'API Aspose.Words pour .NET
description: OdsoRecipientData propriété. Spécifie la colonne de la source de données qui contient des données uniques pour lenregistrement actuel. La valeur par défaut est 0.
type: docs
weight: 30
url: /fr/net/aspose.words.settings/odsorecipientdata/column/
---
## OdsoRecipientData.Column property

Spécifie la colonne de la source de données qui contient des données uniques pour l'enregistrement actuel. La valeur par défaut est 0.

```csharp
public int Column { get; set; }
```

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

// Nous pouvons également supprimer des éléments individuellement ou effacer toute la collection en même temps.
dataCollection.RemoveAt(0);

Assert.AreEqual(69, dataCollection.Count);

dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### Voir également

* class [OdsoRecipientData](../)
* espace de noms [Aspose.Words.Settings](../../odsorecipientdata/)
* Assemblée [Aspose.Words](../../../)


