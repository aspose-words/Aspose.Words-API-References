---
title: FieldMergingArgsBase.FieldValue
second_title: Aspose.Words för .NET API Referens
description: FieldMergingArgsBase fast egendom. Hämtar eller ställer in fältets värde från datakällan.
type: docs
weight: 50
url: /sv/net/aspose.words.mailmerging/fieldmergingargsbase/fieldvalue/
---
## FieldMergingArgsBase.FieldValue property

Hämtar eller ställer in fältets värde från datakällan.

```csharp
public object FieldValue { get; set; }
```

### Anmärkningar

Den här egenskapen innehåller ett värde som just har valts från din datakälla för det här fältet av kopplingsmotorn. Du kan också ersätta värdet genom att ställa in egenskapen.

### Exempel

Visar hur man redigerar värden som MERGEFIELDs tar emot när en e-postsammanslagning sker.

```csharp
public void FieldFormats()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Infoga några MERGEFIELDs med formatväxlar som kommer att redigera de värden de kommer att få under en e-postkoppling.
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
/// Redigerar värdena som MERGEFIELDs får under en e-postkoppling.
/// Namnet på ett MERGEFIELD måste ha ett prefix för att denna callback ska träda i kraft på dess värde.
/// </summary>
private class FieldValueMergingCallback : IFieldMergingCallback
{
    /// <summary>
    /// Anropas när en e-postsammanfogning slår samman data till ett MERGEFIELD.
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
        // Göra ingenting.
    }
}
```

### Se även

* class [FieldMergingArgsBase](../)
* namnutrymme [Aspose.Words.MailMerging](../../fieldmergingargsbase/)
* hopsättning [Aspose.Words](../../../)


