---
title: FieldDocVariable Class
linktitle: FieldDocVariable
articleTitle: FieldDocVariable
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Fields.FieldDocVariable för sömlös DOCVARIABLE-fältintegration, vilket förbättrar din dokumentautomation och -hantering.
type: docs
weight: 2230
url: /sv/net/aspose.words.fields/fielddocvariable/
---
## FieldDocVariable class

Implementerar DOCVARIABLE-fältet.

För att lära dig mer, besök[Arbeta med fält](https://docs.aspose.com/words/net/working-with-fields/) dokumentationsartikel.

```csharp
public class FieldDocVariable : Field
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [FieldDocVariable](fielddocvariable/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Hämtar texten som representerar det visade fältresultatet. |
| [End](../../aspose.words.fields/field/end/) { get; } | Hämtar noden som representerar fältets slut. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Får en[`FieldFormat`](../fieldformat/)objekt som ger typad åtkomst till fältets formatering. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Hämtar eller anger om det aktuella resultatet av fältet inte längre är korrekt (inaktuellt) på grund av andra ändringar som gjorts i dokumentet. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Hämtar eller anger om fältet är låst (resultatet ska inte beräknas om). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Hämtar eller ställer in fältets LCID. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Hämtar eller anger text som är mellan fältavgränsaren och fältslutet. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Hämtar noden som representerar fältseparatorn. Kan vara`null` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Hämtar noden som representerar början av fältet. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Hämtar fälttypen Microsoft Word. |
| [VariableName](../../aspose.words.fields/fielddocvariable/variablename/) { get; set; } | Hämtar eller anger namnet på dokumentvariabeln som ska hämtas. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). Både fältkod och fältresultat för underfält inkluderas. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). |
| [Remove](../../aspose.words.fields/field/remove/)() | Tar bort fältet från dokumentet. Returnerar en nod direkt efter fältet. Om fältets slut är den sista undernoden till dess överordnade nod, returneras dess överordnade stycke. Om fältet redan är borttaget returneras`null` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Utför fältavkopplingen. |
| [Update](../../aspose.words.fields/field/update/)() | Utför fältuppdateringen. Körs om fältet redan uppdateras. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Utför en fältuppdatering. Körs om fältet redan uppdateras. |

## Exempel

Visar hur man använder DOCPROPERTY-fält för att visa dokumentegenskaper och variabler.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nedan följer två sätt att använda DOCPROPERTY-fält.
// 1 - Visa en inbyggd egenskap:
// Ange ett anpassat värde för den inbyggda egenskapen "Kategori" och infoga sedan ett DOCPROPERTY-fält som refererar till det.
doc.BuiltInDocumentProperties.Category = "My category";

FieldDocProperty fieldDocProperty = (FieldDocProperty)builder.InsertField(" DOCPROPERTY Category ");
fieldDocProperty.Update();

Assert.AreEqual(" DOCPROPERTY Category ", fieldDocProperty.GetFieldCode());
Assert.AreEqual("My category", fieldDocProperty.Result);

builder.InsertParagraph();

// 2 - Visa en anpassad dokumentvariabel:
// Definiera en anpassad variabel och referera sedan till den variabeln med ett DOCPROPERTY-fält.
Assert.AreEqual(0, doc.Variables.Count);
doc.Variables.Add("My variable", "My variable's value");

FieldDocVariable fieldDocVariable = (FieldDocVariable)builder.InsertField(FieldType.FieldDocVariable, true);
fieldDocVariable.VariableName = "My Variable";
fieldDocVariable.Update();

Assert.AreEqual(" DOCVARIABLE  \"My Variable\"", fieldDocVariable.GetFieldCode());
Assert.AreEqual("My variable's value", fieldDocVariable.Result);

doc.Save(ArtifactsDir + "Field.DOCPROPERTY.DOCVARIABLE.docx");
```

### Se även

* class [Field](../field/)
* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)
