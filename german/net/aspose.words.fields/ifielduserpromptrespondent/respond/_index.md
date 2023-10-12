---
title: IFieldUserPromptRespondent.Respond
second_title: Aspose.Words für .NET-API-Referenz
description: IFieldUserPromptRespondent methode. Gibt bei Implementierung eine Antwort des Benutzers auf Aufforderung zurück. Ihre Implementierung sollte zurückgegeben werdenNull um anzuzeigen dass der Benutzer nicht auf die Eingabeaufforderung geantwortet hat d. h. der Benutzer hat im Eingabeaufforderungsfenster auf die Schaltfläche Abbrechen geklickt.
type: docs
weight: 10
url: /de/net/aspose.words.fields/ifielduserpromptrespondent/respond/
---
## IFieldUserPromptRespondent.Respond method

Gibt bei Implementierung eine Antwort des Benutzers auf Aufforderung zurück. Ihre Implementierung sollte zurückgegeben werden`Null` um anzuzeigen, dass der Benutzer nicht auf die Eingabeaufforderung geantwortet hat (d. h. der Benutzer hat im Eingabeaufforderungsfenster auf die Schaltfläche „Abbrechen“ geklickt).

```csharp
public string Respond(string promptText, string defaultResponse)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| promptText | String | Eingabeaufforderungstext (z. B. Titel des Eingabeaufforderungsfensters). |
| defaultResponse | String | Standardmäßige Benutzerantwort (dh der im Eingabeaufforderungsfenster enthaltene Anfangswert). |

### Rückgabewert

Benutzerantwort (dh bestätigter Wert im Eingabeaufforderungsfenster).

### Beispiele

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

    // Fügen Sie das ASK-Feld ein und bearbeiten Sie seine Eigenschaften, um unser REF-Feld über den Lesezeichennamen zu referenzieren.
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
    // was während eines Seriendrucks auftreten wird.
    doc.FieldOptions.UserPromptRespondent = new MyPromptRespondent();
    doc.MailMerge.Execute(table);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.ASK.docx");
}

/// <summary>
/// Fügt der Standardantwort eines ASK-Felds während eines Seriendrucks Text voran.
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

* interface [IFieldUserPromptRespondent](../)
* namensraum [Aspose.Words.Fields](../../ifielduserpromptrespondent/)
* Montage [Aspose.Words](../../../)


