---
title: FieldCreateDate.UseUmAlQuraCalendar
second_title: Référence de l'API Aspose.Words pour .NET
description: FieldCreateDate propriété. Obtient ou définit sil faut utiliser le calendrier UmalQura.
type: docs
weight: 40
url: /fr/net/aspose.words.fields/fieldcreatedate/useumalquracalendar/
---
## FieldCreateDate.UseUmAlQuraCalendar property

Obtient ou définit s'il faut utiliser le calendrier Um-al-Qura.

```csharp
public bool UseUmAlQuraCalendar { get; set; }
```

### Exemples

Montre comment utiliser le champ CREATEDATE pour afficher la date/heure de création du document.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.Writeln(" Date this document was created:");

// On peut utiliser le champ CREATEDATE pour afficher la date et l'heure de création du document.
// Vous trouverez ci-dessous trois types de calendrier différents selon lesquels le champ CREATEDATE peut afficher la date/heure.
// 1 - Calendrier Lunaire Islamique :
builder.Write("According to the Lunar Calendar - ");
FieldCreateDate field = (FieldCreateDate)builder.InsertField(FieldType.FieldCreateDate, true);
field.UseLunarCalendar = true;

Assert.AreEqual(" CREATEDATE  \\h", field.GetFieldCode());

// 2 - Calendrier Umm al-Qura :
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
* espace de noms [Aspose.Words.Fields](../../fieldcreatedate/)
* Assemblée [Aspose.Words](../../../)


