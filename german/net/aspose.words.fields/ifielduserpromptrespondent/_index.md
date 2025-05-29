---
title: IFieldUserPromptRespondent Interface
linktitle: IFieldUserPromptRespondent
articleTitle: IFieldUserPromptRespondent
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aspose.Words.Fields.IFieldUserPromptRespondent-Schnittstelle, die entwickelt wurde, um die Benutzerinteraktion zu verbessern und Feldaktualisierungen nahtlos zu optimieren.
type: docs
weight: 3150
url: /de/net/aspose.words.fields/ifielduserpromptrespondent/
---
## IFieldUserPromptRespondent interface

Stellt den Antwortenden auf Benutzeraufforderungen während der Feldaktualisierung dar.

```csharp
public interface IFieldUserPromptRespondent
```

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Respond](../../aspose.words.fields/ifielduserpromptrespondent/respond/)(*string, string*) | Wenn implementiert, gibt es auf Nachfrage eine Antwort vom Benutzer zurück. Ihre Implementierung sollte zurückgeben`null` um anzuzeigen, dass der Benutzer nicht auf die Eingabeaufforderung reagiert hat (d. h. der Benutzer hat im Eingabeaufforderungsfenster auf die Schaltfläche „Abbrechen“ geklickt). |

## Bemerkungen

Die Felder ASK und FILLIN sind Beispiele für Felder, die den Benutzer zu einer Antwort auffordern. Implementieren Sie diese Schnittstelle und weisen Sie sie dem[`UserPromptRespondent`](../fieldoptions/userpromptrespondent/) Eigenschaft zum Herstellen einer Interaktion zwischen dem Feld update und dem Benutzer.

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

* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)
