---
title: FieldAsk.PromptText
linktitle: PromptText
articleTitle: PromptText
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie die FieldAsk-PromptText-Eigenschaft einfach verwalten können, um den Titel Ihres Eingabeaufforderungsfensters für ein verbessertes Benutzererlebnis anzupassen.
type: docs
weight: 50
url: /de/net/aspose.words.fields/fieldask/prompttext/
---
## FieldAsk.PromptText property

Ruft den Eingabeaufforderungstext (den Titel des Eingabeaufforderungsfensters) ab oder legt ihn fest.

```csharp
public string PromptText { get; set; }
```

## Beispiele

Zeigt, wie ein ASK-Feld erstellt und seine Eigenschaften festgelegt werden.

```csharp
public void FieldAsk()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Platzieren Sie ein Feld, in dem die Antwort auf unser ASK-Feld platziert wird.
    FieldRef fieldRef = (FieldRef)builder.InsertField(FieldType.FieldRef, true);
    fieldRef.BookmarkName = "MyAskField";
    builder.Writeln();

    Assert.AreEqual(" REF  MyAskField", fieldRef.GetFieldCode());

    // Fügen Sie das ASK-Feld ein und bearbeiten Sie seine Eigenschaften, um über den Lesezeichennamen auf unser REF-Feld zu verweisen.
    FieldAsk fieldAsk = (FieldAsk)builder.InsertField(FieldType.FieldAsk, true);
    fieldAsk.BookmarkName = "MyAskField";
    fieldAsk.PromptText = "Please provide a response for this ASK field";
    fieldAsk.DefaultResponse = "Response from within the field.";
    fieldAsk.PromptOnceOnMailMerge = true;
    builder.Writeln();

    Assert.AreEqual(
        " ASK  MyAskField \"Please provide a response for this ASK field\" \\d \"Response from within the field.\" \\o",
        fieldAsk.GetFieldCode());

    // ASK-Felder wenden während eines Seriendrucks die Standardantwort auf ihre jeweiligen REF-Felder an.
    DataTable table = new DataTable("My Table");
    table.Columns.Add("Column 1");
    table.Rows.Add("Row 1");
    table.Rows.Add("Row 2");

    FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
    fieldMergeField.FieldName = "Column 1";

    // Wir können die Standardantwort in unseren ASK-Feldern mit einem benutzerdefinierten Prompt-Responder ändern oder überschreiben.
    // was während eines Serienbriefs geschieht.
    doc.FieldOptions.UserPromptRespondent = new MyPromptRespondent();
    doc.MailMerge.Execute(table);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.ASK.docx");
}

/// <summary>
/// Fügt während einer Serienbrieffunktion der Standardantwort eines ASK-Felds Text voran.
/// </summary>
private class MyPromptRespondent : IFieldUserPromptRespondent
{
    public string Respond(string promptText, string defaultResponse)
    {
        return "Response from MyPromptRespondent. " + defaultResponse;
    }
}
```

### Siehe auch

* class [FieldAsk](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
