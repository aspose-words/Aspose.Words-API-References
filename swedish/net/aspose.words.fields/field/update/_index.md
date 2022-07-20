---
title: Update
second_title: Aspose.Words för .NET API Referens
description: Utför fältuppdateringen. Kastar om fältet redan uppdateras.
type: docs
weight: 140
url: /sv/net/aspose.words.fields/field/update/
---
## Update() {#update}

Utför fältuppdateringen. Kastar om fältet redan uppdateras.

```csharp
public void Update()
```

### Exempel

Visar hur man infogar ett fält i ett dokument med hjälp av FieldType.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga två fält samtidigt som du skickar en flagga som avgör om de ska uppdateras när byggaren infogar dem.
// I vissa fall kan det vara beräkningsdyrt att uppdatera fält och det kan vara en bra idé att skjuta upp uppdateringen.
doc.BuiltInDocumentProperties.Author = "John Doe";
builder.Write("This document was written by ");
builder.InsertField(FieldType.FieldAuthor, updateInsertedFieldsImmediately);

builder.InsertParagraph();
builder.Write("\nThis is page ");
builder.InsertField(FieldType.FieldPage, updateInsertedFieldsImmediately);

Assert.AreEqual(" AUTHOR ", doc.Range.Fields[0].GetFieldCode());
Assert.AreEqual(" PAGE ", doc.Range.Fields[1].GetFieldCode());

if (updateInsertedFieldsImmediately)
{
    Assert.AreEqual("John Doe", doc.Range.Fields[0].Result);
    Assert.AreEqual("1", doc.Range.Fields[1].Result);
}
else
{
    Assert.AreEqual(string.Empty, doc.Range.Fields[0].Result);
    Assert.AreEqual(string.Empty, doc.Range.Fields[1].Result);

    // Vi kommer att behöva uppdatera dessa fält med uppdateringsmetoderna manuellt.
    doc.Range.Fields[0].Update();

    Assert.AreEqual("John Doe", doc.Range.Fields[0].Result);

    doc.UpdateFields();

    Assert.AreEqual("1", doc.Range.Fields[1].Result);
}
```

Visar hur man formaterar fältresultat.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Använd en dokumentbyggare för att infoga ett fält som visar ett resultat utan format.
Field field = builder.InsertField("= 2 + 3");

Assert.AreEqual("= 2 + 3", field.GetFieldCode());
Assert.AreEqual("5", field.Result);

// Vi kan tillämpa ett format på ett fälts resultat med hjälp av fältets egenskaper.
// Nedan finns tre typer av format som vi kan tillämpa på ett fälts resultat.
// 1 - Numeriskt format:
FieldFormat format = field.Format;
format.NumericFormat = "$###.00";
field.Update();

Assert.AreEqual("= 2 + 3 \\# $###.00", field.GetFieldCode());
Assert.AreEqual("$  5.00", field.Result);

// 2 - Datum/tid format:
field = builder.InsertField("DATE");
format = field.Format;
format.DateTimeFormat = "dddd, MMMM dd, yyyy";
field.Update();

Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());
Console.WriteLine($"Today's date, in {format.DateTimeFormat} format:\n\t{field.Result}");

// 3 - Allmänt format:
field = builder.InsertField("= 25 + 33");
format = field.Format;
format.GeneralFormats.Add(GeneralFormat.LowercaseRoman);
format.GeneralFormats.Add(GeneralFormat.Upper);
field.Update();

int index = 0;
using (IEnumerator<GeneralFormat> generalFormatEnumerator = format.GeneralFormats.GetEnumerator())
    while (generalFormatEnumerator.MoveNext())
        Console.WriteLine($"General format index {index++}: {generalFormatEnumerator.Current}");

Assert.AreEqual("= 25 + 33 \\* roman \\* Upper", field.GetFieldCode());
Assert.AreEqual("LVIII", field.Result);
Assert.AreEqual(2, format.GeneralFormats.Count);
Assert.AreEqual(GeneralFormat.LowercaseRoman, format.GeneralFormats[0]);

// Vi kan ta bort våra format för att återställa fältets resultat till dess ursprungliga form.
format.GeneralFormats.Remove(GeneralFormat.LowercaseRoman);
format.GeneralFormats.RemoveAt(0);
Assert.AreEqual(0, format.GeneralFormats.Count);
field.Update();

Assert.AreEqual("= 25 + 33  ", field.GetFieldCode());
Assert.AreEqual("58", field.Result);
Assert.AreEqual(0, format.GeneralFormats.Count);
```

### Se även

* class [Field](../../field)
* namnutrymme [Aspose.Words.Fields](../../field)
* hopsättning [Aspose.Words](../../../)

---

## Update(bool) {#update_1}

Utför en fältuppdatering. Kastar om fältet redan uppdateras.

```csharp
public void Update(bool ignoreMergeFormat)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| ignoreMergeFormat | Boolean | Om`Sann` då överges direkt fältresultatformatering, oavsett MERGEFORMAT-växeln, annars utförs normal uppdatering. |

### Exempel

Visar hur man bevarar eller kasserar INCLUDEPICTURE-fält när ett dokument laddas.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldIncludePicture includePicture = (FieldIncludePicture)builder.InsertField(FieldType.FieldIncludePicture, true);
includePicture.SourceFullName = ImageDir + "Transparent background logo.png";
includePicture.Update(true);

using (MemoryStream docStream = new MemoryStream())
{
    doc.Save(docStream, new OoxmlSaveOptions(SaveFormat.Docx));

    // Vi kan sätta en flagga i ett LoadOptions-objekt för att bestämma om alla INCLUDEPICTURE-fält ska konverteras
    // till bildformer när du laddar ett dokument som innehåller dem.
    LoadOptions loadOptions = new LoadOptions
    {
        PreserveIncludePictureField = preserveIncludePictureField
    };

    doc = new Document(docStream, loadOptions);

    if (preserveIncludePictureField)
    {
        Assert.True(doc.Range.Fields.Any(f => f.Type == FieldType.FieldIncludePicture));

        doc.UpdateFields();
        doc.Save(ArtifactsDir + "Field.PreserveIncludePicture.docx");
    }
    else
    {
        Assert.False(doc.Range.Fields.Any(f => f.Type == FieldType.FieldIncludePicture));
    }
}
```

### Se även

* class [Field](../../field)
* namnutrymme [Aspose.Words.Fields](../../field)
* hopsättning [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
