---
title: OdsoFieldMapData.Clone
second_title: Référence de l'API Aspose.Words pour .NET
description: OdsoFieldMapData méthode. Renvoie un clone profond de cet objet.
type: docs
weight: 60
url: /fr/net/aspose.words.settings/odsofieldmapdata/clone/
---
## OdsoFieldMapData.Clone method

Renvoie un clone profond de cet objet.

```csharp
public OdsoFieldMapData Clone()
```

### Exemples

Montre comment accéder à la collection de données qui mappe les colonnes de la source de données aux champs de fusion.

```csharp
Document doc = new Document(MyDir + "Odso data.docx");

// Cette collection définit comment un publipostage mappera les colonnes d'une source de données
// aux champs prédéfinis MERGEFIELD, ADDRESSBLOCK et GREETINGLINE.
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

// Clonez les éléments de cette collection.
Assert.AreNotEqual(dataCollection[0], dataCollection[0].Clone());

// Utilisez les éléments de la méthode "RemoveAt" individuellement par index.
dataCollection.RemoveAt(0);

Assert.AreEqual(29, dataCollection.Count);

// Utilisez la méthode "Clear" pour effacer toute la collection en une seule fois.
dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### Voir également

* class [OdsoFieldMapData](../)
* espace de noms [Aspose.Words.Settings](../../odsofieldmapdata/)
* Assemblée [Aspose.Words](../../../)


