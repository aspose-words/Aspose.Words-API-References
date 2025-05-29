---
title: FieldDate.UseLastFormat
linktitle: UseLastFormat
articleTitle: UseLastFormat
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété FieldDate UseLastFormat améliore votre flux de travail en conservant le dernier format de date utilisé pour une intégration transparente dans vos applications.
type: docs
weight: 20
url: /fr/net/aspose.words.fields/fielddate/uselastformat/
---
## FieldDate.UseLastFormat property

Obtient ou définit s'il faut utiliser un format utilisé en dernier par l'application d'hébergement lors de l'insertion d'un nouveau champ DATE.

```csharp
public bool UseLastFormat { get; set; }
```

## Exemples

Montre comment utiliser les champs DATE pour afficher les dates selon différents types de calendriers.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Si nous voulons que le texte du document affiche toujours la date correcte, nous pouvons utiliser un champ DATE.
// Vous trouverez ci-dessous trois types de calendriers culturels qu'un champ DATE peut utiliser pour afficher une date.
// 1 - Calendrier lunaire islamique :
FieldDate field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseLunarCalendar = true;
Assert.AreEqual(" DATE  \\h", field.GetFieldCode());
builder.Writeln();

// 2 - Calendrier d'Umm al-Qura :
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseUmAlQuraCalendar = true;
Assert.AreEqual(" DATE  \\u", field.GetFieldCode());
builder.Writeln();

// 3 - Calendrier national indien :
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseSakaEraCalendar = true;
Assert.AreEqual(" DATE  \\s", field.GetFieldCode());
builder.Writeln();

// Insérez un champ DATE et définissez son type de calendrier sur celui utilisé en dernier par l'application hôte.
// Dans Microsoft Word, le type sera le plus récemment utilisé dans la boîte de dialogue Insérer -> Texte -> Date et heure.
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseLastFormat = true;
Assert.AreEqual(" DATE  \\l", field.GetFieldCode());
builder.Writeln();

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.DATE.docx");
```

### Voir également

* class [FieldDate](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
