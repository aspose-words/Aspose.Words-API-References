---
title: FieldMergingArgsBase.FieldValue
linktitle: FieldValue
articleTitle: FieldValue
second_title: Aspose.Words för .NET
description: Upptäck FieldValue-egenskapen i FieldMergingArgsBase. Få enkelt åtkomst till och ändra fältvärden från din datakälla för förbättrad datahantering.
type: docs
weight: 50
url: /sv/net/aspose.words.mailmerging/fieldmergingargsbase/fieldvalue/
---
## FieldMergingArgsBase.FieldValue property

Hämtar eller anger värdet för fältet från datakällan.

```csharp
public object FieldValue { get; set; }
```

## Anmärkningar

Den här egenskapen innehåller ett värde som just har valts från din datakälla för det här fältet av dokumentkopplingsmotorn. Du kan också ersätta värdet genom att ange egenskapen.

## Exempel

Visar hur man redigerar värden som MERGEFIELDs tar emot när en dokumentkoppling sker.

```csharp
public void FieldFormats()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Infoga några MERGEFIELDS med formatväxlar som redigerar värdena de får under en dokumentkoppling.
    builder.InsertField("MERGEFIELD text_Field1 \\* Caps", null);
    builder.Write(", ");
    builder.InsertField("MERGEFIELD text_Field2 \\* Upper", null);
    builder.Write(", ");
    builder.InsertField("MERGEFIELD numeric_Field1 \\# 0.0", null);

    builder.Document.MailMerge.FieldMergingCallback = new FieldValueMergingCallback();

    builder.Document.MailMerge.Execute(
        new string[] { "text_Field1", "text_Field2", "numeric_Field1" },
        new object[] { "Field 1", "Field 2", 10 });
    string t = doc.GetText().Trim();
    Assert.AreEqual("Merge Value For \"Text_Field1\": Field 1, MERGE VALUE FOR \"TEXT_FIELD2\": FIELD 2, 10000.0", doc.GetText().Trim());
}

/// <summary>
/// Redigerar värdena som MERGEFIELDs tar emot under en dokumentkoppling.
/// Namnet på ett MERGEFIELD måste ha ett prefix för att denna återanropning ska påverka dess värde.
/// </summary>
private class FieldValueMergingCallback : IFieldMergingCallback
{
    /// <summary>
    /// Anropas när en dokumentkoppling sammanfogar data till ett MERGEFIELD.
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs e)
    {
        if (e.FieldName.StartsWith("text_"))
            e.FieldValue = $"Merge value for \"{e.FieldName}\": {(string)e.FieldValue}";
        else if (e.FieldName.StartsWith("numeric_"))
            e.FieldValue = (int)e.FieldValue * 1000;
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs e)
    {
        // Gör ingenting.
    }
}
```

### Se även

* class [FieldMergingArgsBase](../)
* namnutrymme [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../../)
