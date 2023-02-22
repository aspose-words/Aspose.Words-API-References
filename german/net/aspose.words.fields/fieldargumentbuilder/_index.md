---
title: Class FieldArgumentBuilder
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Fields.FieldArgumentBuilder klas. Erstellt ein komplexes Feldargument das aus Feldern Knoten und Klartext besteht.
type: docs
weight: 1400
url: /de/net/aspose.words.fields/fieldargumentbuilder/
---
## FieldArgumentBuilder class

Erstellt ein komplexes Feldargument, das aus Feldern, Knoten und Klartext besteht.

```csharp
public class FieldArgumentBuilder
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [FieldArgumentBuilder](fieldargumentbuilder/)() | Initialisiert eine Instanz von`FieldArgumentBuilder` Klasse. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [AddField](../../aspose.words.fields/fieldargumentbuilder/addfield/)(FieldBuilder) | Fügt ein Feld hinzu, das durch a dargestellt wird[`FieldBuilder`](../fieldbuilder/) zum argument. |
| [AddNode](../../aspose.words.fields/fieldargumentbuilder/addnode/)(Inline) | Fügt dem Argument einen Knoten hinzu. |
| [AddText](../../aspose.words.fields/fieldargumentbuilder/addtext/)(string) | Fügt dem Argument einen Klartext hinzu. |

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


