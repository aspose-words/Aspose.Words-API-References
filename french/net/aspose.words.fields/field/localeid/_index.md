---
title: Field.LocaleId
linktitle: LocaleId
articleTitle: LocaleId
second_title: Aspose.Words pour .NET
description: Gérez facilement la propriété LocaleId de votre champ. Obtenez ou définissez le LCID pour une localisation et une expérience utilisateur optimisées dans vos applications.
type: docs
weight: 60
url: /fr/net/aspose.words.fields/field/localeid/
---
## Field.LocaleId property

Obtient ou définit le LCID du champ.

```csharp
public int LocaleId { get; set; }
```

## Exemples

Montre comment insérer un champ et travailler avec ses paramètres régionaux.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérez un champ DATE, puis imprimez la date à laquelle il s'affichera.
// La culture actuelle de votre fil détermine le formatage de la date.
Field field = builder.InsertField(@"DATE");
Console.WriteLine($"Today's date, as displayed in the \"{CultureInfo.CurrentCulture.EnglishName}\" culture: {field.Result}");

Assert.AreEqual(1033, field.LocaleId);
// Changer la culture de notre thread aura un impact sur le résultat du champ DATE.
// Une autre façon de faire en sorte que le champ DATE affiche une date dans une culture différente est d'utiliser sa propriété LocaleId.
// Cette méthode nous permet d'éviter de modifier la culture du thread pour obtenir cet effet.
doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
CultureInfo de = new CultureInfo("de-DE");
field.LocaleId = de.LCID;
field.Update();

Console.WriteLine($"Today's date, as displayed according to the \"{CultureInfo.GetCultureInfo(field.LocaleId).EnglishName}\" culture: {field.Result}");
```

### Voir également

* class [Field](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
