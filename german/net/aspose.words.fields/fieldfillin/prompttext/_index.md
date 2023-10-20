---
title: FieldFillIn.PromptText
linktitle: PromptText
articleTitle: PromptText
second_title: Aspose.Words für .NET
description: FieldFillIn PromptText eigendom. Ruft den Eingabeaufforderungstext den Titel des Eingabeaufforderungsfensters ab oder legt diesen fest in C#.
type: docs
weight: 40
url: /de/net/aspose.words.fields/fieldfillin/prompttext/
---
## FieldFillIn.PromptText property

Ruft den Eingabeaufforderungstext (den Titel des Eingabeaufforderungsfensters) ab oder legt diesen fest.

```csharp
public string PromptText { get; set; }
```

## Beispiele

Zeigt, wie das FILLIN-Feld verwendet wird, um den Benutzer zu einer Antwort aufzufordern.

```csharp
public void FieldFillIn()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Ein FILLIN-Feld einfügen. Wenn wir dieses Feld in Microsoft Word manuell aktualisieren,
    // es wird uns auffordern, eine Antwort einzugeben. Das Feld zeigt dann die Antwort als Text an.
    FieldFillIn field = (FieldFillIn)builder.InsertField(FieldType.FieldFillIn, true);
    field.PromptText = "Please enter a response:";
    field.DefaultResponse = "A default response.";

    // Wir können diese Felder auch verwenden, um den Benutzer um eine eindeutige Antwort für jede Seite zu bitten
    // erstellt während eines Seriendrucks mit Microsoft Word.
    field.PromptOnceOnMailMerge = true;

    Assert.AreEqual(" FILLIN  \"Please enter a response:\" \\d \"A default response.\" \\o", field.GetFieldCode());

    FieldMergeField mergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
    mergeField.FieldName = "MergeField";

    // Wenn wir einen Seriendruck programmgesteuert durchführen, können wir einen benutzerdefinierten Eingabeaufforderungsantworten verwenden
    // um Antworten für FILLIN-Felder automatisch zu bearbeiten, auf die der Seriendruck stößt.
    doc.FieldOptions.UserPromptRespondent = new PromptRespondent();
    doc.MailMerge.Execute(new [] { "MergeField" }, new object[] { "" });

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.FILLIN.docx");
}

/// <summary>
/// Fügt der Standardantwort jedes FILLIN-Felds während eines Seriendrucks eine Zeile voran.
/// </summary>
private class PromptRespondent : IFieldUserPromptRespondent
{
    public string Respond(string promptText, string defaultResponse)
    {
        return "Response modified by PromptRespondent. " + defaultResponse;
    }
}
```

### Siehe auch

* class [FieldFillIn](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
