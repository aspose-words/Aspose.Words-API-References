---
title: Document.FieldOptions
linktitle: FieldOptions
articleTitle: FieldOptions
second_title: Aspose.Words pour .NET
description: Explorez la propriété Document FieldOptions pour gérer efficacement la gestion des champs. Découvrez des options uniques pour un contrôle et une personnalisation améliorés des documents.
type: docs
weight: 130
url: /fr/net/aspose.words/document/fieldoptions/
---
## Document.FieldOptions property

Obtient un[`FieldOptions`](../../../aspose.words.fields/fieldoptions/) objet qui représente les options permettant de contrôler la gestion des champs dans le document.

```csharp
public FieldOptions FieldOptions { get; }
```

## Exemples

Montre comment spécifier la source de la culture utilisée pour le formatage de la date lors d'une mise à jour de champ ou d'un publipostage.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer deux champs de fusion avec les paramètres régionaux allemands.
builder.Font.LocaleId = new CultureInfo("de-DE").LCID;
builder.InsertField("MERGEFIELD Date1 \\@ \"dddd, d MMMM yyyy\"");
builder.Write(" - ");
builder.InsertField("MERGEFIELD Date2 \\@ \"dddd, d MMMM yyyy\"");

// Définissez la culture actuelle sur l'anglais américain après avoir conservé sa valeur d'origine dans une variable.
CultureInfo currentCulture = Thread.CurrentThread.CurrentCulture;
Thread.CurrentThread.CurrentCulture = new CultureInfo("en-US");

// Cette fusion utilisera la culture du thread actuel pour formater la date, en anglais américain.
doc.MailMerge.Execute(new[] { "Date1" }, new object[] { new DateTime(2020, 1, 01) });

// Configurez la fusion suivante pour que sa valeur de culture soit issue du code du champ. La valeur de cette culture sera allemande.
doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
doc.MailMerge.Execute(new[] { "Date2" }, new object[] { new DateTime(2020, 1, 01) });

// Le premier résultat de fusion contient une date formatée en anglais, tandis que le second est en allemand.
Assert.AreEqual("Wednesday, 1 January 2020 - Mittwoch, 1 Januar 2020", doc.Range.Text.Trim());

// Restaurer la culture d'origine du thread.
Thread.CurrentThread.CurrentCulture = currentCulture;
```

### Voir également

* class [FieldOptions](../../../aspose.words.fields/fieldoptions/)
* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
