---
title: Class FieldIncludePicture
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Fields.FieldIncludePicture klass. Implementerar fältet INCLUDEPICTURE.
type: docs
weight: 1890
url: /sv/net/aspose.words.fields/fieldincludepicture/
---
## FieldIncludePicture class

Implementerar fältet INCLUDEPICTURE.

```csharp
public class FieldIncludePicture : Field
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [FieldIncludePicture](fieldincludepicture/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Hämtar texten som representerar det visade fältresultatet. |
| [End](../../aspose.words.fields/field/end/) { get; } | Hämtar noden som representerar fältänden. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Får en[`FieldFormat`](../fieldformat/) objekt som ger maskinskriven åtkomst till fältets formatering. |
| [GraphicFilter](../../aspose.words.fields/fieldincludepicture/graphicfilter/) { get; set; } | Hämtar eller ställer in namnet på filtret för formatet på grafiken som ska infogas. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Hämtar eller ställer in om det aktuella resultatet av fältet inte längre är korrekt (inaktuellt) på grund av andra ändringar som gjorts i dokumentet. |
| [IsLinked](../../aspose.words.fields/fieldincludepicture/islinked/) { get; set; } | Hämtar eller ställer in om filstorleken ska minskas genom att inte lagra grafikdata med dokumentet. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Hämtar eller ställer in om fältet är låst (ska inte räkna om resultatet). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Hämtar eller ställer in LCID för fältet. |
| [ResizeHorizontally](../../aspose.words.fields/fieldincludepicture/resizehorizontally/) { get; set; } | Hämtar eller ställer in om storleken på bilden ska ändras horisontellt från källan. |
| [ResizeVertically](../../aspose.words.fields/fieldincludepicture/resizevertically/) { get; set; } | Hämtar eller ställer in om bilden ska ändras vertikalt från källan. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Hämtar eller ställer in text som är mellan fältavgränsaren och fältslutet. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Hämtar noden som representerar fältseparatorn. Kan vara null. |
| [SourceFullName](../../aspose.words.fields/fieldincludepicture/sourcefullname/) { get; set; } | Hämtar eller ställer in bildens plats med en IRI. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Hämtar noden som representerar början av fältet. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Hämtar fälttypen Microsoft Word. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). Både fältkod och fältresultat för underordnade fält ingår. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). |
| [Remove](../../aspose.words.fields/field/remove/)() | Tar bort fältet från dokumentet. Returnerar en nod direkt efter fältet. Om fältets slut är den sista child av dess överordnade nod, returnerar dess överordnade stycke. Om fältet redan är borttaget, returneras **null** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Utför fältavlänkningen. |
| [Update](../../aspose.words.fields/field/update/)() | Utför fältuppdateringen. Kastar om fältet redan uppdateras. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Utför en fältuppdatering. Kastar om fältet redan uppdateras. |

### Anmärkningar

Hämtar en bild och visar den som fältresultat.

### Exempel

Visar hur man infogar bilder med hjälp av IMPORT- och INCLUDEPICTURE-fälten.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nedan finns två liknande fälttyper som vi kan använda för att visa bilder länkade från det lokala filsystemet.
// 1 - Fältet INKLUDERA BILD:
FieldIncludePicture fieldIncludePicture = (FieldIncludePicture)builder.InsertField(FieldType.FieldIncludePicture, true);
fieldIncludePicture.SourceFullName = ImageDir + "Transparent background logo.png";

Assert.True(Regex.Match(fieldIncludePicture.GetFieldCode(), " INCLUDEPICTURE  .*").Success);

// Använd PNG32.FLT-filtret.
fieldIncludePicture.GraphicFilter = "PNG32";
fieldIncludePicture.IsLinked = true;
fieldIncludePicture.ResizeHorizontally = true;
fieldIncludePicture.ResizeVertically = true;

// 2 - IMPORT-fältet:
FieldImport fieldImport = (FieldImport)builder.InsertField(FieldType.FieldImport, true);
fieldImport.SourceFullName = ImageDir + "Transparent background logo.png";
fieldImport.GraphicFilter = "PNG32";
fieldImport.IsLinked = true;

Assert.True(Regex.Match(fieldImport.GetFieldCode(), " IMPORT  .* \\\\c PNG32 \\\\d").Success);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.IMPORT.INCLUDEPICTURE.docx");
```

### Se även

* class [Field](../field/)
* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)


