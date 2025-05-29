---
title: Odso.FieldMapDatas
linktitle: FieldMapDatas
articleTitle: FieldMapDatas
second_title: Aspose.Words pour .NET
description: Découvrez Odso FieldMapDatas, mappez sans effort des colonnes de données externes à des champs de fusion prédéfinis, garantissant une intégration transparente des documents et une précision améliorée des données.
type: docs
weight: 50
url: /fr/net/aspose.words.settings/odso/fieldmapdatas/
---
## Odso.FieldMapDatas property

Obtient ou définit une collection d'objets qui spécifient comment les colonnes de la source de données externe sont mappées aux noms de champs de fusion prédéfinis dans le document. Cet objet n'est jamais`nul` .

```csharp
public OdsoFieldMapDataCollection FieldMapDatas { get; set; }
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

* class [OdsoFieldMapDataCollection](../../odsofieldmapdatacollection/)
* class [Odso](../)
* espace de noms [Aspose.Words.Settings](../../../aspose.words.settings/)
* Assemblée [Aspose.Words](../../../)
