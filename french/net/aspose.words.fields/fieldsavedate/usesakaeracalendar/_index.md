---
title: FieldSaveDate.UseSakaEraCalendar
linktitle: UseSakaEraCalendar
articleTitle: UseSakaEraCalendar
second_title: Aspose.Words pour .NET
description: Gérez vos dates facilement grâce au calendrier Saka Era de FieldSaveDate. Modifiez facilement les paramètres pour un suivi et une organisation optimisés.
type: docs
weight: 30
url: /fr/net/aspose.words.fields/fieldsavedate/usesakaeracalendar/
---
## FieldSaveDate.UseSakaEraCalendar property

Obtient ou définit s'il faut utiliser le calendrier de l'ère Saka.

```csharp
public bool UseSakaEraCalendar { get; set; }
```

## Exemples

Montre comment utiliser le champ SAVEDATE pour afficher la date/heure de la dernière opération d'enregistrement du document effectuée à l'aide de Microsoft Word.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.Writeln(" Date this document was last saved:");

// Nous pouvons utiliser le champ SAVEDATE pour afficher la date et l'heure de la dernière opération de sauvegarde sur le document.
// L'opération de sauvegarde à laquelle ces champs font référence est la sauvegarde manuelle dans une application comme Microsoft Word,
// pas la méthode Save du document.
// Vous trouverez ci-dessous trois types de calendrier différents selon lesquels le champ SAVEDATE peut afficher la date/heure.
// 1 - Calendrier lunaire islamique :
builder.Write("According to the Lunar Calendar - ");
FieldSaveDate field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseLunarCalendar = true;

Assert.AreEqual(" SAVEDATE  \\h", field.GetFieldCode());

// 2 - Calendrier d'Umm al-Qura :
builder.Write("\nAccording to the Umm al-Qura calendar - ");
field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseUmAlQuraCalendar = true;

Assert.AreEqual(" SAVEDATE  \\u", field.GetFieldCode());

// 3 - Calendrier national indien :
builder.Write("\nAccording to the Indian National calendar - ");
field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseSakaEraCalendar = true;

Assert.AreEqual(" SAVEDATE  \\s", field.GetFieldCode());

// Les champs SAVEDATE tirent leurs valeurs de date/heure de la propriété intégrée LastSavedTime.
// La méthode Save du document ne mettra pas à jour cette valeur, mais nous pouvons toujours la mettre à jour manuellement.
doc.BuiltInDocumentProperties.LastSavedTime = DateTime.Now;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SAVEDATE.docx");
```

### Voir également

* class [FieldSaveDate](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
