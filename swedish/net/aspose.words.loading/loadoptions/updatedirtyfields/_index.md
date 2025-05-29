---
title: LoadOptions.UpdateDirtyFields
linktitle: UpdateDirtyFields
articleTitle: UpdateDirtyFields
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen LoadOptions UpdateDirtyFields förbättrar dataintegriteten genom att selektivt uppdatera fält markerade som dirty för optimal prestanda.
type: docs
weight: 160
url: /sv/net/aspose.words.loading/loadoptions/updatedirtyfields/
---
## LoadOptions.UpdateDirtyFields property

Anger om fälten ska uppdateras med`smutsig` attribut.

```csharp
public bool UpdateDirtyFields { get; set; }
```

## Exempel

Visar hur man använder en specialegenskap för att uppdatera fältresultat.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ange dokumentets inbyggda egenskapsvärde "Author" och visa det sedan med ett fält.
doc.BuiltInDocumentProperties.Author = "John Doe";
FieldAuthor field = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);

Assert.False(field.IsDirty);
Assert.AreEqual("John Doe", field.Result);

// Uppdatera egenskapen. Fältet visar fortfarande det gamla värdet.
doc.BuiltInDocumentProperties.Author = "John & Jane Doe";

Assert.AreEqual("John Doe", field.Result);

// Eftersom fältets värde är föråldrat kan vi markera det som "smutsigt".
// Detta värde förblir inaktuellt tills vi uppdaterar fältet manuellt med metoden Field.Update().
field.IsDirty = true;

using (MemoryStream docStream = new MemoryStream())
{
    // Om vi sparar utan att anropa en uppdateringsmetod,
    // fältet kommer att fortsätta visa det föråldrade värdet i utdatadokumentet.
    doc.Save(docStream, SaveFormat.Docx);

    // LoadOptions-objektet har ett alternativ för att uppdatera alla fält
    // markerad som "smutsig" när dokumentet laddades.
    LoadOptions options = new LoadOptions();
    options.UpdateDirtyFields = updateDirtyFields;
    doc = new Document(docStream, options);

    Assert.AreEqual("John & Jane Doe", doc.BuiltInDocumentProperties.Author);

    field = (FieldAuthor)doc.Range.Fields[0];

    // Uppdatering av smutsiga fält som detta sätter automatiskt deras "IsDirty"-flagga till falskt.
    if (updateDirtyFields)
    {
        Assert.AreEqual("John & Jane Doe", field.Result);
        Assert.False(field.IsDirty);
    }
    else
    {
        Assert.AreEqual("John Doe", field.Result);
        Assert.True(field.IsDirty);
    }
}
```

### Se även

* class [LoadOptions](../)
* namnutrymme [Aspose.Words.Loading](../../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../../)
