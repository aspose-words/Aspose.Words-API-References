---
title: FieldFillIn.DefaultResponse
second_title: Aspose.Words för .NET API Referens
description: FieldFillIn fast egendom. Hämtar eller ställer in standardanvändarsvar initialvärde i promptfönstret.
type: docs
weight: 20
url: /sv/net/aspose.words.fields/fieldfillin/defaultresponse/
---
## FieldFillIn.DefaultResponse property

Hämtar eller ställer in standardanvändarsvar (initialvärde i promptfönstret).

```csharp
public string DefaultResponse { get; set; }
```

### Exempel

Visar hur man använder FILLIN-fältet för att fråga användaren om ett svar.

```csharp
public void FieldFillIn()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Infoga ett FILLIN-fält. När vi manuellt uppdaterar detta fält i Microsoft Word,
    // det kommer att uppmana oss att ange ett svar. Fältet kommer då att visa svaret som text.
    FieldFillIn field = (FieldFillIn)builder.InsertField(FieldType.FieldFillIn, true);
    field.PromptText = "Please enter a response:";
    field.DefaultResponse = "A default response.";

    // Vi kan också använda dessa fält för att be användaren om ett unikt svar för varje sida
    // skapad under en sammanfogning med Microsoft Word.
    field.PromptOnceOnMailMerge = true;

    Assert.AreEqual(" FILLIN  \"Please enter a response:\" \\d \"A default response.\" \\o", field.GetFieldCode());

    FieldMergeField mergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
    mergeField.FieldName = "MergeField";

    // Om vi utför en e-postsammankoppling programmatiskt kan vi använda en anpassad svarsfråga
    // för att automatiskt redigera svar för FILLIN-fält som sammanslagningen stöter på.
    doc.FieldOptions.UserPromptRespondent = new PromptRespondent();
    doc.MailMerge.Execute(new [] { "MergeField" }, new object[] { "" });

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.FILLIN.docx");
}

/// <summary>
/// Lägger en rad till standardsvaret för varje FILLIN-fält under en e-postkoppling.
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
* namnutrymme [Aspose.Words.Fields](../../fieldfillin/)
* hopsättning [Aspose.Words](../../../)


