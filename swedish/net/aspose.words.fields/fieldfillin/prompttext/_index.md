---
title: FieldFillIn.PromptText
linktitle: PromptText
articleTitle: PromptText
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FieldFillIn PromptText och anpassa enkelt titlar på promptfönster för att förbättra användarupplevelsen och förbättra gränssnittets tydlighet.
type: docs
weight: 40
url: /sv/net/aspose.words.fields/fieldfillin/prompttext/
---
## FieldFillIn.PromptText property

Hämtar eller ställer in prompttexten (titeln på promptfönstret).

```csharp
public string PromptText { get; set; }
```

## Exempel

Visar hur man använder FILLIN-fältet för att uppmana användaren att svara.

```csharp
public void FieldFillIn()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Infoga ett FILLIN-fält. När vi manuellt uppdaterar detta fält i Microsoft Word,
    // det kommer att uppmana oss att ange ett svar. Fältet kommer sedan att visa svaret som text.
    FieldFillIn field = (FieldFillIn)builder.InsertField(FieldType.FieldFillIn, true);
    field.PromptText = "Please enter a response:";
    field.DefaultResponse = "A default response.";

    // Vi kan också använda dessa fält för att be användaren om ett unikt svar för varje sida
    // skapades under en dokumentkoppling som gjordes med Microsoft Word.
    field.PromptOnceOnMailMerge = true;

    Assert.AreEqual(" FILLIN  \"Please enter a response:\" \\d \"A default response.\" \\o", field.GetFieldCode());

    FieldMergeField mergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
    mergeField.FieldName = "MergeField";

    // Om vi utför en dokumentkoppling programmatiskt kan vi använda en anpassad promptsvarare
    // för att automatiskt redigera svar för FILLIN-fält som dokumentkopplingen stöter på.
    doc.FieldOptions.UserPromptRespondent = new PromptRespondent();
    doc.MailMerge.Execute(new [] { "MergeField" }, new object[] { "" });

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.FILLIN.docx");
}

/// <summary>
/// Lägger till en rad före standardsvaret för varje FILLIN-fält under en dokumentkoppling.
/// </summary>
private class PromptRespondent : IFieldUserPromptRespondent
{
    public string Respond(string promptText, string defaultResponse)
    {
        return "Response modified by PromptRespondent. " + defaultResponse;
    }
}
```

### Se även

* class [FieldFillIn](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
