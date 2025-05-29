---
title: FieldOptions.LegacyNumberFormat
linktitle: LegacyNumberFormat
articleTitle: LegacyNumberFormat
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FieldOptions LegacyNumberFormat för att aktivera eller inaktivera äldre talformat för fält, vilket förbättrar kompatibilitet och prestanda.
type: docs
weight: 160
url: /sv/net/aspose.words.fields/fieldoptions/legacynumberformat/
---
## FieldOptions.LegacyNumberFormat property

Hämtar eller ställer in värdet som anger om äldre (tidigare än AW 13.10) talformat för fält är aktiverat eller inte.

```csharp
public bool LegacyNumberFormat { get; set; }
```

## Anmärkningar

När den här egenskapen är inställd på`sann`, mallsymbolen "#" fungerade som i .net: Ersätter pundtecknet med motsvarande siffra om en sådan finns; annars visas inga symboler i resultatsträngen.

När den här egenskapen är inställd på`falsk`, mallsymbolen "#" fungerar som MS Word: Detta formatobjekt anger de numeriska tecken som ska visas i resultatet. Om resultatet inte innehåller en siffra på den platsen visar MS Word ett mellanslag. Till exempel visar { = 9 + 6 \# $### } $ 15.

Standardvärdet är`falsk`.

## Exempel

Visar hur man aktiverar äldre talformatering för fält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("= 2 + 3 \\# $##");

Assert.AreEqual("$ 5", field.Result);

doc.FieldOptions.LegacyNumberFormat = true;
field.Update();

Assert.AreEqual("$5", field.Result);
```

### Se även

* class [FieldOptions](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
