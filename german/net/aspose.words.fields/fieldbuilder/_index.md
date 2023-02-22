---
title: Class FieldBuilder
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Fields.FieldBuilder klas. Erstellt ein Feld aus FeldcodeTokens Argumente und Schalter.
type: docs
weight: 1510
url: /de/net/aspose.words.fields/fieldbuilder/
---
## FieldBuilder class

Erstellt ein Feld aus Feldcode-Tokens (Argumente und Schalter).

```csharp
public class FieldBuilder
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [FieldBuilder](fieldbuilder/)(FieldType) | Initialisiert eine Instanz von`FieldBuilder` Klasse. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [AddArgument](../../aspose.words.fields/fieldbuilder/addargument/#addargument_2)(double) | Fügt das Argument eines Felds hinzu. |
| [AddArgument](../../aspose.words.fields/fieldbuilder/addargument/#addargument)(FieldArgumentBuilder) | Fügt das Argument eines Feldes hinzu, dargestellt durch[`FieldArgumentBuilder`](../fieldargumentbuilder/) zum Feldcode. |
| [AddArgument](../../aspose.words.fields/fieldbuilder/addargument/#addargument_1)(FieldBuilder) | Fügt ein untergeordnetes Feld hinzu, das durch ein anderes repräsentiert wird`FieldBuilder` zum Feldcode. |
| [AddArgument](../../aspose.words.fields/fieldbuilder/addargument/#addargument_3)(int) | Fügt das Argument eines Felds hinzu. |
| [AddArgument](../../aspose.words.fields/fieldbuilder/addargument/#addargument_4)(string) | Fügt das Argument eines Felds hinzu. |
| [AddSwitch](../../aspose.words.fields/fieldbuilder/addswitch/#addswitch)(string) | Fügt einen Feldschalter hinzu. |
| [AddSwitch](../../aspose.words.fields/fieldbuilder/addswitch/#addswitch_1)(string, double) | Fügt einen Feldschalter hinzu. |
| [AddSwitch](../../aspose.words.fields/fieldbuilder/addswitch/#addswitch_2)(string, int) | Fügt einen Feldschalter hinzu. |
| [AddSwitch](../../aspose.words.fields/fieldbuilder/addswitch/#addswitch_3)(string, string) | Fügt einen Feldschalter hinzu. |
| [BuildAndInsert](../../aspose.words.fields/fieldbuilder/buildandinsert/#buildandinsert)(Inline) | Erstellt ein Feld und fügt es vor dem angegebenen Inline-Knoten in das Dokument ein. |
| [BuildAndInsert](../../aspose.words.fields/fieldbuilder/buildandinsert/#buildandinsert_1)(Paragraph) | Erstellt ein Feld und fügt es bis zum Ende des angegebenen Absatzes in das Dokument ein. |

### Beispiele

Zeigt, wie Felder mit einem Feldgenerator erstellt und dann in das Dokument eingefügt werden.

```csharp
Document doc = new Document();

// Unten sind drei Beispiele für die Feldkonstruktion mit einem Feldgenerator.
// 1 - Einzelfeld:
// Verwenden Sie einen Feldgenerator, um ein SYMBOL-Feld hinzuzufügen, das das Symbol ƒ (Florin) anzeigt.
FieldBuilder builder = new FieldBuilder(FieldType.FieldSymbol);
builder.AddArgument(402);
builder.AddSwitch("\\f", "Arial");
builder.AddSwitch("\\s", 25);
builder.AddSwitch("\\u");
Field field = builder.BuildAndInsert(doc.FirstSection.Body.FirstParagraph);

Assert.AreEqual(" SYMBOL 402 \\f Arial \\s 25 \\u ", field.GetFieldCode());

// 2 - Verschachteltes Feld:
// Verwenden Sie einen Feldgenerator, um ein Formelfeld zu erstellen, das von einem anderen Feldgenerator als inneres Feld verwendet wird.
FieldBuilder innerFormulaBuilder = new FieldBuilder(FieldType.FieldFormula);
innerFormulaBuilder.AddArgument(100);
innerFormulaBuilder.AddArgument("+");
innerFormulaBuilder.AddArgument(74);

// Einen weiteren Builder für ein weiteres SYMBOL-Feld erstellen und das Formelfeld einfügen
 // die wir oben erstellt haben, in das Feld SYMBOL als Argument.
builder = new FieldBuilder(FieldType.FieldSymbol);
builder.AddArgument(innerFormulaBuilder);
field = builder.BuildAndInsert(doc.FirstSection.Body.AppendParagraph(string.Empty));

// Das äußere Feld SYMBOL verwendet das Ergebnis des Formelfelds, 174, als Argument,
// wodurch das Feld das Symbol ® (Registered Sign) anzeigt, da seine Zeichennummer 174 ist.
Assert.AreEqual(" SYMBOL \u0013 = 100 + 74 \u0014\u0015 ", field.GetFieldCode());

// 3 - Mehrere verschachtelte Felder und Argumente:
// Jetzt verwenden wir einen Builder, um ein IF-Feld zu erstellen, das einen von zwei benutzerdefinierten Zeichenfolgenwerten anzeigt,
// abhängig vom wahren/falschen Wert seines Ausdrucks. Um einen True/False-Wert zu erhalten
// die bestimmt, welche Zeichenfolge das IF-Feld anzeigt, testet das IF-Feld zwei numerische Ausdrücke auf Gleichheit.
// Wir werden die beiden Ausdrücke in Form von Formelfeldern bereitstellen, die wir innerhalb des IF-Felds verschachteln.
FieldBuilder leftExpression = new FieldBuilder(FieldType.FieldFormula);
leftExpression.AddArgument(2);
leftExpression.AddArgument("+");
leftExpression.AddArgument(3);

FieldBuilder rightExpression = new FieldBuilder(FieldType.FieldFormula);
rightExpression.AddArgument(2.5);
rightExpression.AddArgument("*");
rightExpression.AddArgument(5.2);

// Als Nächstes erstellen wir zwei Feldargumente, die als Wahr/Falsch-Ausgabestrings für das IF-Feld dienen.
// Diese Argumente werden die Ausgabewerte unserer numerischen Ausdrücke wiederverwenden.
FieldArgumentBuilder trueOutput = new FieldArgumentBuilder();
trueOutput.AddText("True, both expressions amount to ");
trueOutput.AddField(leftExpression);

FieldArgumentBuilder falseOutput = new FieldArgumentBuilder();
falseOutput.AddNode(new Run(doc, "False, "));
falseOutput.AddField(leftExpression);
falseOutput.AddNode(new Run(doc, " does not equal "));
falseOutput.AddField(rightExpression);

 // Schließlich erstellen wir einen weiteren Feldgenerator für das IF-Feld und kombinieren alle Ausdrücke.
builder = new FieldBuilder(FieldType.FieldIf);
builder.AddArgument(leftExpression);
builder.AddArgument("=");
builder.AddArgument(rightExpression);
builder.AddArgument(trueOutput);
builder.AddArgument(falseOutput);
field = builder.BuildAndInsert(doc.FirstSection.Body.AppendParagraph(string.Empty));

Assert.AreEqual(" IF \u0013 = 2 + 3 \u0014\u0015 = \u0013 = 2.5 * 5.2 \u0014\u0015 " +
                "\"True, both expressions amount to \u0013 = 2 + 3 \u0014\u0015\" " +
                "\"False, \u0013 = 2 + 3 \u0014\u0015 does not equal \u0013 = 2.5 * 5.2 \u0014\u0015\" ", field.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SYMBOL.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)


