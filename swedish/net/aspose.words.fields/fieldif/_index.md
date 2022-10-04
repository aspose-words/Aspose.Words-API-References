---
title: FieldIf
second_title: Aspose.Words för .NET API Referens
description: Implementerar IFfältet.
type: docs
weight: 1850
url: /sv/net/aspose.words.fields/fieldif/
---
## FieldIf class

Implementerar IF-fältet.

```csharp
public class FieldIf : Field
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [FieldIf](fieldif/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [ComparisonOperator](../../aspose.words.fields/fieldif/comparisonoperator/) { get; set; } | Hämtar eller ställer in jämförelseoperatorn. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Hämtar texten som representerar det visade fältresultatet. |
| [End](../../aspose.words.fields/field/end/) { get; } | Hämtar noden som representerar fältänden. |
| [FalseText](../../aspose.words.fields/fieldif/falsetext/) { get; set; } | Hämtar eller ställer in texten som visas om jämförelseuttrycket är falskt. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Får en[`FieldFormat`](../fieldformat/) objekt som ger maskinskriven åtkomst till fältets formatering. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Hämtar eller ställer in om det aktuella resultatet av fältet inte längre är korrekt (inaktuellt) på grund av andra ändringar som gjorts i dokumentet. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Hämtar eller ställer in om fältet är låst (ska inte räkna om resultatet). |
| [LeftExpression](../../aspose.words.fields/fieldif/leftexpression/) { get; set; } | Hämtar eller ställer in den vänstra delen av jämförelseuttrycket. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Hämtar eller ställer in LCID för fältet. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Hämtar eller ställer in text som är mellan fältavgränsaren och fältslutet. |
| [RightExpression](../../aspose.words.fields/fieldif/rightexpression/) { get; set; } | Hämtar eller ställer in den högra delen av jämförelseuttrycket. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Hämtar noden som representerar fältseparatorn. Kan vara null. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Hämtar noden som representerar början av fältet. |
| [TrueText](../../aspose.words.fields/fieldif/truetext/) { get; set; } | Hämtar eller ställer in texten som visas om jämförelseuttrycket är sant. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Hämtar fälttypen Microsoft Word. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [EvaluateCondition](../../aspose.words.fields/fieldif/evaluatecondition/)() | Utvärderar villkoret. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). Både fältkod och fältresultat för underordnade fält ingår. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). |
| [Remove](../../aspose.words.fields/field/remove/)() | Tar bort fältet från dokumentet. Returnerar en nod direkt efter fältet. Om fältets slut är den sista child av dess överordnade nod, returnerar dess överordnade stycke. Om fältet redan är borttaget, returneras **null** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Utför fältavlänkningen. |
| [Update](../../aspose.words.fields/field/update/)() | Utför fältuppdateringen. Kastar om fältet redan uppdateras. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Utför en fältuppdatering. Kastar om fältet redan uppdateras. |

### Anmärkningar

Jämför värdena som anges av uttrycken[`LeftExpression`](./leftexpression/) och[`RightExpression`](./rightexpression/) i jämförelse med den operatör som anges av[`ComparisonOperator`](./comparisonoperator/).

Ett fält i följande format kommer att användas som en kopplingskälla: { IF 0 = 0 "{PatientsNameFML}" "" \* MERGEFORMAT }

### Exempel

Visar hur man infogar ett IF-fält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Statement 1: ");
FieldIf field = (FieldIf)builder.InsertField(FieldType.FieldIf, true);
field.LeftExpression = "0";
field.ComparisonOperator = "=";
field.RightExpression = "1";

// IF-fältet kommer att visa en sträng från antingen dess "TrueText"-egenskap,
// eller dess "FalseText"-egenskap, beroende på sanningen i påståendet som vi har konstruerat.
field.TrueText = "True";
field.FalseText = "False";
field.Update();

// I det här fallet är "0 = 1" felaktigt, så det visade resultatet blir "False".
Assert.AreEqual(" IF  0 = 1 True False", field.GetFieldCode());
Assert.AreEqual(FieldIfComparisonResult.False, field.EvaluateCondition());
Assert.AreEqual("False", field.Result);

builder.Write("\nStatement 2: ");
field = (FieldIf)builder.InsertField(FieldType.FieldIf, true);
field.LeftExpression = "5";
field.ComparisonOperator = "=";
field.RightExpression = "2 + 3";
field.TrueText = "True";
field.FalseText = "False";
field.Update();

// Den här gången är påståendet korrekt, så det visade resultatet blir "True".
Assert.AreEqual(" IF  5 = \"2 + 3\" True False", field.GetFieldCode());
Assert.AreEqual(FieldIfComparisonResult.True, field.EvaluateCondition());
Assert.AreEqual("True", field.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.IF.docx");
```

### Se även

* class [Field](../field/)
* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
