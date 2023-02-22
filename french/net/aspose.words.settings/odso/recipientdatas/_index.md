---
title: Odso.RecipientDatas
second_title: Référence de l'API Aspose.Words pour .NET
description: Odso propriété. Obtient ou définit une collection dobjets qui spécifient linclusion/exclusion denregistrements individuels dans le publipostage. Cet objet nest jamais null.
type: docs
weight: 70
url: /fr/net/aspose.words.settings/odso/recipientdatas/
---
## Odso.RecipientDatas property

Obtient ou définit une collection d'objets qui spécifient l'inclusion/exclusion d'enregistrements individuels dans le publipostage. Cet objet n'est jamais null.

```csharp
public OdsoRecipientDataCollection RecipientDatas { get; set; }
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

// Nous pouvons également supprimer des éléments individuellement ou effacer toute la collection en une seule fois.
dataCollection.RemoveAt(0);

Assert.AreEqual(69, dataCollection.Count);

dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### Voir également

* class [OdsoRecipientDataCollection](../../odsorecipientdatacollection/)
* class [Odso](../)
* espace de noms [Aspose.Words.Settings](../../odso/)
* Assemblée [Aspose.Words](../../../)


