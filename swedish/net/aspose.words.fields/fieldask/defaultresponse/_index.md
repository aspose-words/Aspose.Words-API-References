---
title: FieldAsk.DefaultResponse
linktitle: DefaultResponse
articleTitle: DefaultResponse
second_title: Aspose.Words för .NET
description: FieldAsk DefaultResponse fast egendom. Hämtar eller ställer in standardanvändarsvar initialvärde i promptfönstret i C#.
type: docs
weight: 30
url: /sv/net/aspose.words.fields/fieldask/defaultresponse/
---
## FieldAsk.DefaultResponse property

Hämtar eller ställer in standardanvändarsvar (initialvärde i promptfönstret).

```csharp
public string DefaultResponse { get; set; }
```

## Exempel

Visar hur man skapar ett ASK-fält och ställer in dess egenskaper.

```csharp
public void FieldAsk()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Placera ett fält där svaret på vårt ASK-fält kommer att placeras.
    FieldRef fieldRef = (FieldRef)builder.InsertField(FieldType.FieldRef, true);
    fieldRef.BookmarkName = "MyAskField";
    builder.Writeln();

    Assert.AreEqual(" REF  MyAskField", fieldRef.GetFieldCode());

    // Infoga ASK-fältet och redigera dess egenskaper för att referera till vårt REF-fält med bokmärkesnamn.
    FieldAsk fieldAsk = (FieldAsk)builder.InsertField(FieldType.FieldAsk, true);
    fieldAsk.BookmarkName = "MyAskField";
    fieldAsk.PromptText = "Please provide a response for this ASK field";
    fieldAsk.DefaultResponse = "Response from within the field.";
    fieldAsk.PromptOnceOnMailMerge = true;
    builder.Writeln();

    Assert.AreEqual(
        " ASK  MyAskField \"Please provide a response for this ASK field\" \\d \"Response from within the field.\" \\o",
        fieldAsk.GetFieldCode());

    // ASK-fält tillämpar standardsvaret på sina respektive REF-fält under en e-postkoppling.
    DataTable table = new DataTable("My Table");
    table.Columns.Add("Column 1");
    table.Rows.Add("Row 1");
    table.Rows.Add("Row 2");

    FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
    fieldMergeField.FieldName = "Column 1";

    // Vi kan ändra eller åsidosätta standardsvaret i våra ASK-fält med en anpassad promptsvarare,
    // som kommer att inträffa under en e-postkoppling.
    doc.FieldOptions.UserPromptRespondent = new MyPromptRespondent();
    doc.MailMerge.Execute(table);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.ASK.docx");
}

/// <summary>
/// Lägger text framför standardsvaret i ett ASK-fält under en e-postkoppling.
/// </summary>
private class MyPromptRespondent : IFieldUserPromptRespondent
{
    public string Respond(string promptText, string defaultResponse)
    {
        return "Response from MyPromptRespondent. " + defaultResponse;
    }
}
```

### Se även

* class [FieldAsk](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
