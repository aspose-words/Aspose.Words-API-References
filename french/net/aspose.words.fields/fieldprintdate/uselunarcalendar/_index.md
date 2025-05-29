---
title: FieldPrintDate.UseLunarCalendar
linktitle: UseLunarCalendar
articleTitle: UseLunarCalendar
second_title: Aspose.Words pour .NET
description: Gérez facilement les dates grâce à la propriété UseLunarCalendar de FieldPrintDate. Basculez facilement entre les calendriers lunaires hégirien et hébreu pour une intégration fluide.
type: docs
weight: 20
url: /fr/net/aspose.words.fields/fieldprintdate/uselunarcalendar/
---
## FieldPrintDate.UseLunarCalendar property

Obtient ou définit s'il faut utiliser le calendrier lunaire hégirien ou lunaire hébreu.

```csharp
public bool UseLunarCalendar { get; set; }
```

## Exemples

Affiche les champs PRINTDATE lus.

```csharp
Document doc = new Document(MyDir + "Field sample - PRINTDATE.docx");

// Lorsqu'un document est imprimé par une imprimante ou imprimé au format PDF (mais pas exporté au format PDF),
// Les champs PRINTDATE afficheront la date/heure de l'opération d'impression.
// Si aucune impression n'a eu lieu, ces champs afficheront « 0/0/0000 ».
FieldPrintDate field = (FieldPrintDate)doc.Range.Fields[0];

Assert.AreEqual("3/25/2020 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE ", field.GetFieldCode());

// Vous trouverez ci-dessous trois types de calendrier différents selon lesquels le champ PRINTDATE
// peut afficher la date et l'heure de la dernière opération d'impression.
// 1 - Calendrier lunaire islamique :
field = (FieldPrintDate)doc.Range.Fields[1];

Assert.True(field.UseLunarCalendar);
Assert.AreEqual("8/1/1441 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE  \\h", field.GetFieldCode());

field = (FieldPrintDate)doc.Range.Fields[2];

// 2 - Calendrier d'Umm al-Qura :
Assert.True(field.UseUmAlQuraCalendar);
Assert.AreEqual("8/1/1441 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE  \\u", field.GetFieldCode());

field = (FieldPrintDate)doc.Range.Fields[3];

// 3 - Calendrier national indien :
Assert.True(field.UseSakaEraCalendar);
Assert.AreEqual("1/5/1942 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE  \\s", field.GetFieldCode());
```

### Voir également

* class [FieldPrintDate](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
