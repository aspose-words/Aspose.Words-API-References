---
title: Class FieldTime
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Fields.FieldTime klass. Implementerar fältet TIME.
type: docs
weight: 2500
url: /sv/net/aspose.words.fields/fieldtime/
---
## FieldTime class

Implementerar fältet TIME.

För att lära dig mer, besök[Arbeta med Fields](https://docs.aspose.com/words/net/working-with-fields/) dokumentationsartikel.

```csharp
public class FieldTime : Field
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [FieldTime](fieldtime/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Hämtar texten som representerar det visade fältresultatet. |
| [End](../../aspose.words.fields/field/end/) { get; } | Hämtar noden som representerar fältänden. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Får en[`FieldFormat`](../fieldformat/) objekt som ger maskinskriven åtkomst till fältets formatering. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Hämtar eller ställer in om det aktuella resultatet av fältet inte längre är korrekt (inaktuellt) på grund av andra ändringar som gjorts i dokumentet. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Hämtar eller ställer in om fältet är låst (ska inte räkna om resultatet). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Hämtar eller ställer in LCID för fältet. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Hämtar eller ställer in text som är mellan fältavgränsaren och fältslutet. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Hämtar noden som representerar fältseparatorn. Kan vara`null` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Hämtar noden som representerar början av fältet. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Hämtar fälttypen Microsoft Word. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). Både fältkod och fältresultat för underordnade fält ingår. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). |
| [Remove](../../aspose.words.fields/field/remove/)() | Tar bort fältet från dokumentet. Returnerar en nod direkt efter fältet. Om fältets slut är den sista child av dess överordnade nod, returnerar dess överordnade stycke. Om fältet redan är borttaget, returneras`null` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Utför fältavlänkningen. |
| [Update](../../aspose.words.fields/field/update/)() | Utför fältuppdateringen. Kastar om fältet redan uppdateras. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Utför en fältuppdatering. Kastar om fältet redan uppdateras. |

### Anmärkningar

Infogar aktuellt datum och tid.

### Exempel

Visar hur man visar aktuell tid med hjälp av TIME-fältet.

```csharp
public void FieldTime()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Som standard visas tiden i formatet "h:mm am/pm".
    FieldTime field = InsertFieldTime(builder, "");

    Assert.AreEqual(" TIME ", field.GetFieldCode());

    // Vi kan använda flaggan \@ för att ändra formatet på vår visade tid.
    field = InsertFieldTime(builder, "\\@ HHmm");

    Assert.AreEqual(" TIME \\@ HHmm", field.GetFieldCode());

    // Vi kan justera formatet för att få TID-fältet för att även visa datumet, enligt den gregorianska kalendern.
    field = InsertFieldTime(builder, "\\@ \"M/d/yyyy h mm:ss am/pm\"");

    Assert.AreEqual(" TIME \\@ \"M/d/yyyy h mm:ss am/pm\"", field.GetFieldCode());

    doc.Save(ArtifactsDir + "Field.TIME.docx");
}

/// <summary>
/// Använd en dokumentbyggare för att infoga ett TID-fält, infoga ett nytt stycke och returnera fältet.
/// </summary>
private static FieldTime InsertFieldTime(DocumentBuilder builder, string format)
{
    FieldTime field = (FieldTime)builder.InsertField(FieldType.FieldTime, true);
    builder.MoveTo(field.Separator);
    builder.Write(format);
    builder.MoveTo(field.Start.ParentNode);

    builder.InsertParagraph();
    return field;
}
```

### Se även

* class [Field](../field/)
* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)


