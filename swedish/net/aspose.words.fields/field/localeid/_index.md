---
title: Field.LocaleId
linktitle: LocaleId
articleTitle: LocaleId
second_title: Aspose.Words för .NET
description: Hantera ditt fälts LocaleId-egenskap enkelt. Hämta eller ställ in LCID för förbättrad lokalisering och användarupplevelse i dina applikationer.
type: docs
weight: 60
url: /sv/net/aspose.words.fields/field/localeid/
---
## Field.LocaleId property

Hämtar eller ställer in fältets LCID.

```csharp
public int LocaleId { get; set; }
```

## Exempel

Visar hur man infogar ett fält och arbetar med dess språkinställning.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga ett DATUM-fält och skriv sedan ut datumet som ska visas.
// Din tråds nuvarande kultur avgör formateringen av datumet.
Field field = builder.InsertField(@"DATE");
Console.WriteLine($"Today's date, as displayed in the \"{CultureInfo.CurrentCulture.EnglishName}\" culture: {field.Result}");

Assert.AreEqual(1033, field.LocaleId);
// Att ändra trådkulturen kommer att påverka resultatet av DATE-fältet.
// Ett annat sätt att få DATE-fältet att visa ett datum i en annan kultur är att använda dess LocaleId-egenskap.
// På detta sätt kan vi undvika att ändra trådens kultur för att få denna effekt.
doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
CultureInfo de = new CultureInfo("de-DE");
field.LocaleId = de.LCID;
field.Update();

Console.WriteLine($"Today's date, as displayed according to the \"{CultureInfo.GetCultureInfo(field.LocaleId).EnglishName}\" culture: {field.Result}");
```

### Se även

* class [Field](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
