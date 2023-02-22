---
title: Enum FieldUpdateCultureSource
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Fields.FieldUpdateCultureSource énumération. Indique quelle culture utiliser lors de la mise à jour du champ.
type: docs
weight: 2410
url: /fr/net/aspose.words.fields/fieldupdateculturesource/
---
## FieldUpdateCultureSource enumeration

Indique quelle culture utiliser lors de la mise à jour du champ.

```csharp
public enum FieldUpdateCultureSource
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| CurrentThread | `0` | La culture du thread d'exécution en cours est utilisée pour mettre à jour les champs. |
| FieldCode | `1` | La culture spécifiée dans les propriétés de mise en forme du champ via le paramètre de langue est utilisée. |

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

// Cette fusion utilisera la culture du thread actuel pour formater la date, en anglais américain.
doc.MailMerge.Execute(new[] { "Date1" }, new object[] { new DateTime(2020, 1, 01) });

// Configurez la prochaine fusion pour obtenir sa valeur de culture à partir du code de champ. La valeur de cette culture sera l'allemand.
doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
doc.MailMerge.Execute(new[] { "Date2" }, new object[] { new DateTime(2020, 1, 01) });

// Le premier résultat de fusion contient une date formatée en anglais, tandis que le second est en allemand.
Assert.AreEqual("Wednesday, 1 January 2020 - Mittwoch, 1 Januar 2020", doc.Range.Text.Trim());

// Restaure la culture d'origine du thread.
Thread.CurrentThread.CurrentCulture = currentCulture;
```

### Voir également

* espace de noms [Aspose.Words.Fields](../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../)


