---
title: IFieldUserPromptRespondent.Respond
linktitle: Respond
articleTitle: Respond
second_title: Aspose.Words för .NET
description: Upptäck metoden iFieldUserPromptRespondent Respond för att effektivt samla in användarsvar. Lär dig hur du hanterar avbokningar smidigt!
type: docs
weight: 10
url: /sv/net/aspose.words.fields/ifielduserpromptrespondent/respond/
---
## IFieldUserPromptRespondent.Respond method

Returnerar ett svar från användaren vid en fråga när den är implementerad. Din implementering ska returnera`null` för att indikera att användaren inte har svarat på prompten (dvs. användaren har tryckt på knappen Avbryt i promptfönstret).

```csharp
public string Respond(string promptText, string defaultResponse)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| promptText | String | Prompttext (dvs. titel på promptfönstret). |
| defaultResponse | String | Standardanvändarsvar (dvs. initialvärde som finns i promptfönstret). |

### Returvärde

Användarsvar (dvs. bekräftat värde i meddelandefönstret).

## Exempel

Visar hur man skapar ett ASK-fält och anger dess egenskaper.

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

    // ASK-fält tillämpar standardsvaret på sina respektive REF-fält under en dokumentkoppling.
    DataTable table = new DataTable("My Table");
    table.Columns.Add("Column 1");
    table.Rows.Add("Row 1");
    table.Rows.Add("Row 2");

    FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
    fieldMergeField.FieldName = "Column 1";

    // Vi kan ändra eller åsidosätta standardsvaret i våra ASK-fält med en anpassad promptresponder,
    // vilket kommer att inträffa under en dokumentkoppling.
    doc.FieldOptions.UserPromptRespondent = new MyPromptRespondent();
    doc.MailMerge.Execute(table);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.ASK.docx");
}

/// <summary>
/// Lägger till text före standardsvaret i ett ASK-fält under en dokumentkoppling.
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

* interface [IFieldUserPromptRespondent](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
