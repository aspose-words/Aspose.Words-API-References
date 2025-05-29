---
title: FieldFillIn.PromptOnceOnMailMerge
linktitle: PromptOnceOnMailMerge
articleTitle: PromptOnceOnMailMerge
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihren Serienbrief mit der Eigenschaft PromptOnceOnMailMerge. Steuern Sie Benutzerreaktionen für eine effiziente Datenerfassung in Ihren Dokumenten.
type: docs
weight: 30
url: /de/net/aspose.words.fields/fieldfillin/promptonceonmailmerge/
---
## FieldFillIn.PromptOnceOnMailMerge property

Ruft ab oder legt fest, ob die Benutzerantwort einmal pro Serienbriefvorgang empfangen werden soll.

```csharp
public bool PromptOnceOnMailMerge { get; set; }
```

## Beispiele

Zeigt, wie das Feld FILLIN verwendet wird, um den Benutzer zur Eingabe einer Antwort aufzufordern.

```csharp
public void FieldFillIn()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Füge ein FILLIN-Feld ein. Wenn wir dieses Feld in Microsoft Word manuell aktualisieren,
    // Wir werden aufgefordert, eine Antwort einzugeben. Das Feld zeigt die Antwort dann als Text an.
    FieldFillIn field = (FieldFillIn)builder.InsertField(FieldType.FieldFillIn, true);
    field.PromptText = "Please enter a response:";
    field.DefaultResponse = "A default response.";

    // Wir können diese Felder auch verwenden, um den Benutzer für jede Seite um eine eindeutige Antwort zu bitten
    // erstellt während eines Serienbriefs mit Microsoft Word.
    field.PromptOnceOnMailMerge = true;

    Assert.AreEqual(" FILLIN  \"Please enter a response:\" \\d \"A default response.\" \\o", field.GetFieldCode());

    FieldMergeField mergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
    mergeField.FieldName = "MergeField";

    // Wenn wir einen Serienbrief programmgesteuert durchführen, können wir einen benutzerdefinierten Prompt-Antwortenden verwenden
    // um Antworten für FILLIN-Felder, die beim Seriendruck gefunden werden, automatisch zu bearbeiten.
    doc.FieldOptions.UserPromptRespondent = new PromptRespondent();
    doc.MailMerge.Execute(new [] { "MergeField" }, new object[] { "" });

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.FILLIN.docx");
}

/// <summary>
/// Fügt während eines Serienbriefs der Standardantwort jedes FILLIN-Felds eine Zeile voran.
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
