---
title: FieldAutoNum.SeparatorCharacter
linktitle: SeparatorCharacter
articleTitle: SeparatorCharacter
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FieldAutoNum SeparatorCharacter och anpassa enkelt ditt avgränsningstecken för förbättrad dataformatering och förbättrad användbarhet.
type: docs
weight: 20
url: /sv/net/aspose.words.fields/fieldautonum/separatorcharacter/
---
## FieldAutoNum.SeparatorCharacter property

Hämtar eller ställer in avgränsartecknet som ska användas.

```csharp
public string SeparatorCharacter { get; set; }
```

## Exempel

Visar hur man numrerar stycken med hjälp av autonumreringsfält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Varje AUTONUMM-fält visar det aktuella värdet av en löpande räkning av AUTONUMM-fält,
// låter oss automatiskt numrera objekt som en numrerad lista.
// Det här fältet visar siffran "1.".
FieldAutoNum field = (FieldAutoNum)builder.InsertField(FieldType.FieldAutoNum, true);
builder.Writeln("\tParagraph 1.");

Assert.AreEqual(" AUTONUM ", field.GetFieldCode());

field = (FieldAutoNum)builder.InsertField(FieldType.FieldAutoNum, true);
builder.Writeln("\tParagraph 2.");

// Avgränsartecknet, som visas i fältresultatet omedelbart efter numret, är som standard en punkt.
// Om vi lämnar den här egenskapen null, kommer vårt andra AUTONUMM-fält att visa "2." i dokumentet.
Assert.IsNull(field.SeparatorCharacter);

// Vi kan ställa in den här egenskapen så att det första tecknet i strängen används som nytt avgränsningstecken.
// I det här fallet kommer vårt AUTONUMM-fält nu att visa "2:".
field.SeparatorCharacter = ":";

Assert.AreEqual(" AUTONUM  \\s :", field.GetFieldCode());

doc.Save(ArtifactsDir + "Field.AUTONUM.docx");
```

### Se även

* class [FieldAutoNum](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
