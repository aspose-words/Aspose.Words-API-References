---
title: OdsoFieldMapDataCollection.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words pour .NET
description: Effacez sans effort votre OdsoFieldMapDataCollection avec notre méthode Clear, garantissant un nouveau départ en supprimant tous les éléments rapidement et efficacement.
type: docs
weight: 50
url: /fr/net/aspose.words.settings/odsofieldmapdatacollection/clear/
---
## OdsoFieldMapDataCollection.Clear method

Supprime tous les éléments de cette collection.

```csharp
public void Clear()
```

## Exemples

Montre comment accéder à la collection de données qui mappe les colonnes de la source de données aux champs de fusion.

```csharp
Document doc = new Document(MyDir + "Odso data.docx");

// Cette collection définit comment un publipostage mappera les colonnes d'une source de données
// aux champs MERGEFIELD, ADDRESSBLOCK et GREETINGLINE prédéfinis.
OdsoFieldMapDataCollection dataCollection = doc.MailMergeSettings.Odso.FieldMapDatas;
Assert.AreEqual(30, dataCollection.Count);

using (IEnumerator<OdsoFieldMapData> enumerator = dataCollection.GetEnumerator())
{
    int index = 0;
    while (enumerator.MoveNext())
    {
        Console.WriteLine($"Field map data index {index++}, type \"{enumerator.Current.Type}\":");

        Console.WriteLine(
            enumerator.Current.Type != OdsoFieldMappingType.Null
                ? $"\tColumn \"{enumerator.Current.Name}\", number {enumerator.Current.Column} mapped to merge field \"{enumerator.Current.MappedName}\"."
                : "\tNo valid column to field mapping data present.");
    }
}

// Cloner les éléments de cette collection.
Assert.AreNotEqual(dataCollection[0], dataCollection[0].Clone());

// Utilisez les éléments de la méthode « RemoveAt » individuellement par index.
dataCollection.RemoveAt(0);

Assert.AreEqual(29, dataCollection.Count);

// Utilisez la méthode « Clear » pour effacer toute la collection en une seule fois.
dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### Voir également

* class [OdsoFieldMapDataCollection](../)
* espace de noms [Aspose.Words.Settings](../../../aspose.words.settings/)
* Assemblée [Aspose.Words](../../../)
