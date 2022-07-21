---
title: FieldIf
second_title: Aspose.Words für .NET-API-Referenz
description: Implementiert das IF-Feld.
type: docs
weight: 1850
url: /de/net/aspose.words.fields/fieldif/
---
## FieldIf class

Implementiert das IF-Feld.

```csharp
public class FieldIf : Field
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [FieldIf](fieldif)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [ComparisonOperator](../../aspose.words.fields/fieldif/comparisonoperator) { get; set; } | Ruft den Vergleichsoperator ab oder setzt ihn. |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Ruft den Text ab, der das angezeigte Feldergebnis darstellt. |
| [End](../../aspose.words.fields/field/end) { get; } | Ruft den Knoten ab, der das Feldende darstellt. |
| [FalseText](../../aspose.words.fields/fieldif/falsetext) { get; set; } | Ruft den angezeigten Text ab oder legt ihn fest, wenn der Vergleichsausdruck falsch ist. |
| [Format](../../aspose.words.fields/field/format) { get; } | erhält a[`FieldFormat`](../fieldformat) Objekt, das typisierten Zugriff auf die Feldformatierung bereitstellt. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer Änderungen am Dokument nicht mehr korrekt (veraltet) ist. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Ruft ab oder legt fest, ob das Feld gesperrt ist (sollte sein Ergebnis nicht neu berechnen). |
| [LeftExpression](../../aspose.words.fields/fieldif/leftexpression) { get; set; } | Ruft den linken Teil des Vergleichsausdrucks ab oder legt ihn fest. |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Ruft die LCID des Felds ab oder legt sie fest. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Liest oder setzt Text, der zwischen dem Feldtrennzeichen und dem Feldende steht. |
| [RightExpression](../../aspose.words.fields/fieldif/rightexpression) { get; set; } | Holt oder setzt den rechten Teil des Vergleichsausdrucks. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Ruft den Knoten ab, der das Feldtrennzeichen darstellt. Kann null sein. |
| [Start](../../aspose.words.fields/field/start) { get; } | Ruft den Knoten ab, der den Anfang des Felds darstellt. |
| [TrueText](../../aspose.words.fields/fieldif/truetext) { get; set; } | Ruft den angezeigten Text ab oder legt ihn fest, wenn der Vergleichsausdruck wahr ist. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Ruft den Microsoft Word-Feldtyp ab. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [EvaluateCondition](../../aspose.words.fields/fieldif/evaluatecondition)() | Wertet die Bedingung aus. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). Sowohl Feldcode als auch Feldergebnis von untergeordneten Feldern sind enthalten. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | Gibt Text zwischen Feldanfang und Feldtrennzeichen (oder Feldende, wenn kein Trennzeichen vorhanden ist) zurück. |
| [Remove](../../aspose.words.fields/field/remove)() | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Felds das letzte Kind seines Elternknotens ist, wird sein Elternabsatz zurückgegeben. Wenn das Feld bereits entfernt wurde, wird zurückgegeben **Null** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | Führt das Feld Unlink aus. |
| [Update](../../aspose.words.fields/field/update)() | Führt die Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |
| [Update](../../aspose.words.fields/field/update)(bool) | Führt eine Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |

### Bemerkungen

Vergleicht die von den Ausdrücken bezeichneten Werte[`LeftExpression`](./leftexpression) und[`RightExpression`](./rightexpression) im Vergleich mit dem von bezeichneten Operator[`ComparisonOperator`](./comparisonoperator).

Als Seriendruckquelle wird ein Feld im folgenden Format verwendet: { IF 0 = 0 "{PatientsNameFML}" "" \* MERGEFORMAT }

### Beispiele

Zeigt, wie ein IF-Feld eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Statement 1: ");
FieldIf field = (FieldIf)builder.InsertField(FieldType.FieldIf, true);
field.LeftExpression = "0";
field.ComparisonOperator = "=";
field.RightExpression = "1";

// Das IF-Feld zeigt einen String entweder aus seiner "TrueText"-Eigenschaft,
// oder seine "FalseText"-Eigenschaft, abhängig von der Wahrheit der von uns konstruierten Aussage.
field.TrueText = "True";
field.FalseText = "False";
field.Update();

// In diesem Fall ist "0 = 1" falsch, daher ist das angezeigte Ergebnis "False".
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

// Diesmal ist die Aussage richtig, also ist das angezeigte Ergebnis "True".
Assert.AreEqual(" IF  5 = \"2 + 3\" True False", field.GetFieldCode());
Assert.AreEqual(FieldIfComparisonResult.True, field.EvaluateCondition());
Assert.AreEqual("True", field.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.IF.docx");
```

### Siehe auch

* class [Field](../field)
* namensraum [Aspose.Words.Fields](../../aspose.words.fields)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
