---
title: GeneralFormatCollection Class
linktitle: GeneralFormatCollection
articleTitle: GeneralFormatCollection
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Fields.GeneralFormatCollection, une collection typée puissante pour gérer sans effort les formats généraux dans vos documents.
type: docs
weight: 3060
url: /fr/net/aspose.words.fields/generalformatcollection/
---
## GeneralFormatCollection class

Représente une collection typée de formats généraux.

Pour en savoir plus, visitez le[Travailler avec les champs](https://docs.aspose.com/words/net/working-with-fields/) article de documentation.

```csharp
public class GeneralFormatCollection : IEnumerable<GeneralFormat>
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words.fields/generalformatcollection/count/) { get; } | Obtient le nombre total d'éléments dans la collection. |
| [Item](../../aspose.words.fields/generalformatcollection/item/) { get; } | Obtient un format général à l'index spécifié. |

## Méthodes

| Nom | La description |
| --- | --- |
| [Add](../../aspose.words.fields/generalformatcollection/add/)(*[GeneralFormat](../generalformat/)*) | Ajoute un format général à la collection. |
| [GetEnumerator](../../aspose.words.fields/generalformatcollection/getenumerator/)() | Renvoie un objet énumérateur. |
| [Remove](../../aspose.words.fields/generalformatcollection/remove/)(*[GeneralFormat](../generalformat/)*) | Supprime toutes les occurrences du format général spécifié de la collection. |
| [RemoveAt](../../aspose.words.fields/generalformatcollection/removeat/)(*int*) | Supprime une occurrence de format général à l'index spécifié. |

## Exemples

Montre comment formater les résultats des champs.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Utilisez un générateur de documents pour insérer un champ qui affiche un résultat sans format appliqué.
Field field = builder.InsertField("= 2 + 3");

Assert.AreEqual("= 2 + 3", field.GetFieldCode());
Assert.AreEqual("5", field.Result);

// Nous pouvons appliquer un format au résultat d'un champ en utilisant les propriétés du champ.
// Vous trouverez ci-dessous trois types de formats que nous pouvons appliquer au résultat d'un champ.
// 1 - Format numérique :
FieldFormat format = field.Format;
format.NumericFormat = "$###.00";
field.Update();

Assert.AreEqual("= 2 + 3 \\# $###.00", field.GetFieldCode());
Assert.AreEqual("$  5.00", field.Result);

// 2 - Format date/heure :
field = builder.InsertField("DATE");
format = field.Format;
format.DateTimeFormat = "dddd, MMMM dd, yyyy";
field.Update();

Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());
Console.WriteLine($"Today's date, in {format.DateTimeFormat} format:\n\t{field.Result}");

// 3 - Format général :
field = builder.InsertField("= 25 + 33");
format = field.Format;
format.GeneralFormats.Add(GeneralFormat.LowercaseRoman);
format.GeneralFormats.Add(GeneralFormat.Upper);
field.Update();

int index = 0;
using (IEnumerator<GeneralFormat> generalFormatEnumerator = format.GeneralFormats.GetEnumerator())
    while (generalFormatEnumerator.MoveNext())
        Console.WriteLine($"General format index {index++}: {generalFormatEnumerator.Current}");

Assert.AreEqual("= 25 + 33 \\* roman \\* Upper", field.GetFieldCode());
Assert.AreEqual("LVIII", field.Result);
Assert.AreEqual(2, format.GeneralFormats.Count);
Assert.AreEqual(GeneralFormat.LowercaseRoman, format.GeneralFormats[0]);

// Nous pouvons supprimer nos formats pour ramener le résultat du champ à sa forme d'origine.
format.GeneralFormats.Remove(GeneralFormat.LowercaseRoman);
format.GeneralFormats.RemoveAt(0);
Assert.AreEqual(0, format.GeneralFormats.Count);
field.Update();

Assert.AreEqual("= 25 + 33  ", field.GetFieldCode());
Assert.AreEqual("58", field.Result);
Assert.AreEqual(0, format.GeneralFormats.Count);
```

### Voir également

* enum [GeneralFormat](../generalformat/)
* espace de noms [Aspose.Words.Fields](../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../)
