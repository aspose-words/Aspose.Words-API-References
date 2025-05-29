---
title: FieldOptions.UseInvariantCultureNumberFormat
linktitle: UseInvariantCultureNumberFormat
articleTitle: UseInvariantCultureNumberFormat
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FieldOptions UseInvariantCultureNumberFormat pour gérer facilement le formatage des nombres avec une culture invariante pour une gestion cohérente des données.
type: docs
weight: 210
url: /fr/net/aspose.words.fields/fieldoptions/useinvariantculturenumberformat/
---
## FieldOptions.UseInvariantCultureNumberFormat property

Obtient ou définit la valeur indiquant que le format du nombre est analysé à l'aide d'une culture invariante ou non

```csharp
public bool UseInvariantCultureNumberFormat { get; set; }
```

## Remarques

Lorsque cette propriété est définie sur`vrai` le format numérique est tiré d'une culture invariante.

Lorsque cette propriété est définie sur`FAUX` , le format numérique est tiré de la culture du thread actuel.

La valeur par défaut est`FAUX`.

## Exemples

Montre comment formater les nombres en fonction de la culture invariante.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Thread.CurrentThread.CurrentCulture = new CultureInfo("de-DE");
Field field = builder.InsertField(" = 1234567,89 \\# $#,###,###.##");
field.Update();

 // Parfois, les champs peuvent ne pas formater correctement leurs nombres dans certaines cultures.
Assert.IsFalse(doc.FieldOptions.UseInvariantCultureNumberFormat);
Assert.AreEqual("$1.234.567,89 ,     ", field.Result);

// Pour résoudre ce problème, nous pourrions changer la culture de l’ensemble du thread.
// Une autre façon de résoudre ce problème est de définir cet indicateur,
// qui oblige tous les champs à utiliser la culture invariante lors du formatage des nombres.
// Cette méthode nous permet d'éviter de changer la culture pour l'ensemble du thread.
doc.FieldOptions.UseInvariantCultureNumberFormat = true;
field.Update();
Assert.AreEqual("$1.234.567,89", field.Result);
```

### Voir également

* class [FieldOptions](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
