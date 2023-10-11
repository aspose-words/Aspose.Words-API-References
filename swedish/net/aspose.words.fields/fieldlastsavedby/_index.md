---
title: Class FieldLastSavedBy
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Fields.FieldLastSavedBy klass. Implementerar fältet LASTSAVEDBY.
type: docs
weight: 2100
url: /sv/net/aspose.words.fields/fieldlastsavedby/
---
## FieldLastSavedBy class

Implementerar fältet LASTSAVEDBY.

För att lära dig mer, besök[Arbeta med Fields](https://docs.aspose.com/words/net/working-with-fields/) dokumentationsartikel.

```csharp
public class FieldLastSavedBy : Field
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [FieldLastSavedBy](fieldlastsavedby/)() | Default_Constructor |

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

Hämtar namnet på den användare som senast ändrade och sparade det aktuella dokumentet, som registrerats i **LastModifiedBy** egenskapen för de inbyggda dokumentegenskaperna.

### Exempel

Visar hur man använder fältet LASTSAVEDBY.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Om vi skapar ett dokument i Microsoft Word kommer det att ha användarens namn i den inbyggda egenskapen "Senast sparad av".
 // Om vi skapar ett dokument programmatiskt kommer den här egenskapen att vara null och vi måste tilldela ett värde.
doc.BuiltInDocumentProperties.LastSavedBy = "John Doe";

// Vi kan använda fältet LASTSAVEDBY för att visa värdet på den här egenskapen i dokumentet.
FieldLastSavedBy field = (FieldLastSavedBy)builder.InsertField(FieldType.FieldLastSavedBy, true);

Assert.AreEqual(" LASTSAVEDBY ", field.GetFieldCode());
Assert.AreEqual("John Doe", field.Result);

doc.Save(ArtifactsDir + "Field.LASTSAVEDBY.docx");
```

### Se även

* class [Field](../field/)
* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)


