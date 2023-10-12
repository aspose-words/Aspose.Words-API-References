---
title: FieldOptions.FieldUpdateCultureSource
second_title: Référence de l'API Aspose.Words pour .NET
description: FieldOptions propriété. Spécifie la culture à utiliser pour formater le résultat du champ.
type: docs
weight: 110
url: /fr/net/aspose.words.fields/fieldoptions/fieldupdateculturesource/
---
## FieldOptions.FieldUpdateCultureSource property

Spécifie la culture à utiliser pour formater le résultat du champ.

```csharp
public FieldUpdateCultureSource FieldUpdateCultureSource { get; set; }
```

### Remarques

Par défaut, la culture du thread actuel est utilisée.

Le paramètre affecte uniquement les champs date/heure avec le commutateur de format \\@.

### Exemples

Montre comment spécifier la source de la culture utilisée pour le formatage de la date lors d'une mise à jour de champ ou d'un publipostage.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère deux champs de fusion avec les paramètres régionaux allemands.
builder.Font.LocaleId = new CultureInfo("de-DE").LCID;
builder.InsertField("MERGEFIELD Date1 \\@ \"dddd, d MMMM yyyy\"");
builder.Write(" - ");
builder.InsertField("MERGEFIELD Date2 \\@ \"dddd, d MMMM yyyy\"");

// Définit la culture actuelle sur l'anglais américain après avoir conservé sa valeur d'origine dans une variable.
CultureInfo currentCulture = Thread.CurrentThread.CurrentCulture;
Thread.CurrentThread.CurrentCulture = new CultureInfo("en-US");

// Cette fusion utilisera la culture du fil de discussion actuel pour formater la date, en anglais américain.
doc.MailMerge.Execute(new[] { "Date1" }, new object[] { new DateTime(2020, 1, 01) });

// Configurez la prochaine fusion pour obtenir sa valeur de culture à partir du code de champ. La valeur de cette culture sera allemande.
doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
doc.MailMerge.Execute(new[] { "Date2" }, new object[] { new DateTime(2020, 1, 01) });

// Le premier résultat de fusion contient une date formatée en anglais, tandis que la seconde est en allemand.
Assert.AreEqual("Wednesday, 1 January 2020 - Mittwoch, 1 Januar 2020", doc.Range.Text.Trim());

// Restaurer la culture d'origine du fil.
Thread.CurrentThread.CurrentCulture = currentCulture;
```

### Voir également

* enum [FieldUpdateCultureSource](../../fieldupdateculturesource/)
* class [FieldOptions](../)
* espace de noms [Aspose.Words.Fields](../../fieldoptions/)
* Assemblée [Aspose.Words](../../../)


