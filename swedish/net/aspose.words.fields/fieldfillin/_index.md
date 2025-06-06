---
title: FieldFillIn Class
linktitle: FieldFillIn
articleTitle: FieldFillIn
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Fields.FieldFillIn-klassen för att enkelt implementera FILLIN-fält, vilket förbättrar din dokumentautomation och användarinteraktivitet.
type: docs
weight: 2300
url: /sv/net/aspose.words.fields/fieldfillin/
---
## FieldFillIn class

Implementerar FILLIN-fältet.

För att lära dig mer, besök[Arbeta med fält](https://docs.aspose.com/words/net/working-with-fields/) dokumentationsartikel.

```csharp
public class FieldFillIn : Field
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [FieldFillIn](fieldfillin/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [DefaultResponse](../../aspose.words.fields/fieldfillin/defaultresponse/) { get; set; } | Hämtar eller ställer in standardanvändarsvar (initialvärde som finns i promptfönstret). |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Hämtar texten som representerar det visade fältresultatet. |
| [End](../../aspose.words.fields/field/end/) { get; } | Hämtar noden som representerar fältets slut. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Får en[`FieldFormat`](../fieldformat/)objekt som ger typad åtkomst till fältets formatering. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Hämtar eller anger om det aktuella resultatet av fältet inte längre är korrekt (inaktuellt) på grund av andra ändringar som gjorts i dokumentet. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Hämtar eller anger om fältet är låst (resultatet ska inte beräknas om). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Hämtar eller ställer in fältets LCID. |
| [PromptOnceOnMailMerge](../../aspose.words.fields/fieldfillin/promptonceonmailmerge/) { get; set; } | Hämtar eller anger om användarsvaret ska tas emot en gång per dokumentkopplingsoperation. |
| [PromptText](../../aspose.words.fields/fieldfillin/prompttext/) { get; set; } | Hämtar eller ställer in prompttexten (titeln på promptfönstret). |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Hämtar eller anger text som är mellan fältavgränsaren och fältslutet. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Hämtar noden som representerar fältseparatorn. Kan vara`null` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Hämtar noden som representerar början av fältet. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Hämtar fälttypen Microsoft Word. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). Både fältkod och fältresultat för underfält inkluderas. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). |
| [Remove](../../aspose.words.fields/field/remove/)() | Tar bort fältet från dokumentet. Returnerar en nod direkt efter fältet. Om fältets slut är den sista undernoden till dess överordnade nod, returneras dess överordnade stycke. Om fältet redan är borttaget returneras`null` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Utför fältavkopplingen. |
| [Update](../../aspose.words.fields/field/update/)() | Utför fältuppdateringen. Körs om fältet redan uppdateras. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Utför en fältuppdatering. Körs om fältet redan uppdateras. |

## Anmärkningar

Uppmanar användaren att ange text.

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

* class [Field](../field/)
* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)
