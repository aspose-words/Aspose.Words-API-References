---
title: FieldOptions.UseInvariantCultureNumberFormat
second_title: Référence de l'API Aspose.Words pour .NET
description: FieldOptions propriété. Obtient ou définit la valeur indiquant que le format numérique est analysé à laide dune culture invariante ou non
type: docs
weight: 190
url: /fr/net/aspose.words.fields/fieldoptions/useinvariantculturenumberformat/
---
## FieldOptions.UseInvariantCultureNumberFormat property

Obtient ou définit la valeur indiquant que le format numérique est analysé à l'aide d'une culture invariante ou non

```csharp
public bool UseInvariantCultureNumberFormat { get; set; }
```

### Remarques

Lorsque cette propriété est définie sur **vrai** , le format numérique est tiré d'une culture invariante.

Lorsque cette propriété est définie sur **faux** le format numérique est extrait de la culture du thread actuel.

La valeur par défaut est **faux**.

### Exemples

Montre comment mettre en forme des nombres en fonction de la culture invariante.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Thread.CurrentThread.CurrentCulture = new CultureInfo("de-DE");
Field field = builder.InsertField(" = 1234567,89 \\# $#,###,###.##");
field.Update();

// Parfois, les champs peuvent ne pas formater correctement leurs nombres dans certaines cultures. 
Assert.IsFalse(doc.FieldOptions.UseInvariantCultureNumberFormat);
Assert.AreEqual("$1234567,89 .     ", field.Result);

// Pour résoudre ce problème, nous pourrions changer la culture de l'ensemble du thread.
// Une autre façon de résoudre ce problème est de définir ce drapeau,
// qui permet à tous les champs d'utiliser la culture invariante lors du formatage des nombres.
// Cette méthode nous permet d'éviter de modifier la culture de l'ensemble du thread.
doc.FieldOptions.UseInvariantCultureNumberFormat = true;
field.Update();
Assert.AreEqual("$1.234.567,89", field.Result);
```

### Voir également

* class [FieldOptions](../)
* espace de noms [Aspose.Words.Fields](../../fieldoptions/)
* Assemblée [Aspose.Words](../../../)


