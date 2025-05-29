---
title: FieldOptions.UseInvariantCultureNumberFormat
linktitle: UseInvariantCultureNumberFormat
articleTitle: UseInvariantCultureNumberFormat
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FieldOptions UseInvariantCultureNumberFormat för att enkelt hantera talformatering med invariant kultur för konsekvent datahantering.
type: docs
weight: 210
url: /sv/net/aspose.words.fields/fieldoptions/useinvariantculturenumberformat/
---
## FieldOptions.UseInvariantCultureNumberFormat property

Hämtar eller ställer in värdet som anger att talformatet analyseras med hjälp av invariant kultur eller inte

```csharp
public bool UseInvariantCultureNumberFormat { get; set; }
```

## Anmärkningar

När den här egenskapen är inställd på`sann` talformatet är hämtat från en invariant kultur.

När den här egenskapen är inställd på`falsk` , talformatet är hämtat från den aktuella trådens kultur.

Standardvärdet är`falsk`.

## Exempel

Visar hur man formaterar tal enligt den invarianta kulturen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Thread.CurrentThread.CurrentCulture = new CultureInfo("de-DE");
Field field = builder.InsertField(" = 1234567,89 \\# $#,###,###.##");
field.Update();

 // Ibland formaterar inte fält sina siffror korrekt under vissa kulturer.
Assert.IsFalse(doc.FieldOptions.UseInvariantCultureNumberFormat);
Assert.AreEqual("$1.234.567,89 ,     ", field.Result);

// För att åtgärda detta kan vi ändra kulturen för hela tråden.
// Ett annat sätt att åtgärda detta är att sätta den här flaggan,
// vilket får alla fält att använda den invarianta kulturen vid formatering av tal.
// På detta sätt undviker vi att ändra kulturen för hela tråden.
doc.FieldOptions.UseInvariantCultureNumberFormat = true;
field.Update();
Assert.AreEqual("$1.234.567,89", field.Result);
```

### Se även

* class [FieldOptions](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
