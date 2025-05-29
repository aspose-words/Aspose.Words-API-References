---
title: FieldCreateDate.UseSakaEraCalendar
linktitle: UseSakaEraCalendar
articleTitle: UseSakaEraCalendar
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FieldCreateDate UseSakaEraCalendar pour gérer facilement les paramètres du calendrier Saka Era dans vos applications pour une gestion améliorée des dates.
type: docs
weight: 30
url: /fr/net/aspose.words.fields/fieldcreatedate/usesakaeracalendar/
---
## FieldCreateDate.UseSakaEraCalendar property

Obtient ou définit s'il faut utiliser le calendrier de l'ère Saka.

```csharp
public bool UseSakaEraCalendar { get; set; }
```

## Exemples

Montre comment utiliser le champ CREATEDATE pour afficher la date/heure de création du document.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.Writeln(" Date this document was created:");

// Nous pouvons utiliser le champ CREATEDATE pour afficher la date et l'heure de création du document.
// Vous trouverez ci-dessous trois types de calendrier différents selon lesquels le champ CREATEDATE peut afficher la date/heure.
// 1 - Calendrier lunaire islamique :
builder.Write("According to the Lunar Calendar - ");
FieldCreateDate field = (FieldCreateDate)builder.InsertField(FieldType.FieldCreateDate, true);
field.UseLunarCalendar = true;

Assert.AreEqual(" CREATEDATE  \\h", field.GetFieldCode());

// 2 - Calendrier d'Umm al-Qura :
builder.Write("\nAccording to the Umm al-Qura Calendar - ");
field = (FieldCreateDate)builder.InsertField(FieldType.FieldCreateDate, true);
field.UseUmAlQuraCalendar = true;

Assert.AreEqual(" CREATEDATE  \\u", field.GetFieldCode());

// 3 - Calendrier national indien :
builder.Write("\nAccording to the Indian National Calendar - ");
field = (FieldCreateDate)builder.InsertField(FieldType.FieldCreateDate, true);
field.UseSakaEraCalendar = true;

Assert.AreEqual(" CREATEDATE  \\s", field.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CREATEDATE.docx");
```

### Voir également

* class [FieldCreateDate](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
