---
title: FieldArgumentBuilder
linktitle: FieldArgumentBuilder
articleTitle: FieldArgumentBuilder
second_title: Aspose.Words für .NET
description: Entdecken Sie den FieldArgumentBuilder-Konstruktor, um FieldArgumentBuilder-Instanzen effizient zu erstellen und an Ihre Entwicklungsanforderungen anzupassen.
type: docs
weight: 10
url: /de/net/aspose.words.fields/fieldargumentbuilder/fieldargumentbuilder/
---
## FieldArgumentBuilder constructor

Initialisiert eine Instanz des[`FieldArgumentBuilder`](../) Klasse.

```csharp
public FieldArgumentBuilder()
```

## Beispiele

Zeigt, wie Sie mit einem Feldgenerator Felder erstellen und diese dann in das Dokument einfügen.

```csharp
Document doc = new Document();

// Nachfolgend finden Sie drei Beispiele für die Feldkonstruktion mithilfe eines Feldgenerators.
// 1 - Einzelnes Feld:
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
    // das wir oben erstellt haben, als Argument in das SYMBOL-Feld ein.
builder = new FieldBuilder(FieldType.FieldSymbol);
builder.AddArgument(innerFormulaBuilder);
field = builder.BuildAndInsert(doc.FirstSection.Body.AppendParagraph(string.Empty));

// Das äußere SYMBOL-Feld verwendet das Formelfeldergebnis 174 als Argument.
// Dadurch wird im Feld das Symbol ® (Registered Sign) angezeigt, da seine Zeichennummer 174 ist.
Assert.AreEqual(" SYMBOL \u0013 = 100 + 74 \u0014\u0015 ", field.GetFieldCode());

// 3 – Mehrere verschachtelte Felder und Argumente:
// Jetzt verwenden wir einen Builder, um ein IF-Feld zu erstellen, das einen von zwei benutzerdefinierten Zeichenfolgenwerten anzeigt.
// abhängig vom Wahr/Falsch-Wert des Ausdrucks. Um einen Wahr/Falsch-Wert zu erhalten
// das bestimmt, welche Zeichenfolge das IF-Feld anzeigt. Das IF-Feld prüft zwei numerische Ausdrücke auf Gleichheit.
// Wir stellen die beiden Ausdrücke in Form von Formelfeldern bereit, die wir in das IF-Feld einbetten.
FieldBuilder leftExpression = new FieldBuilder(FieldType.FieldFormula);
leftExpression.AddArgument(2);
leftExpression.AddArgument("+");
leftExpression.AddArgument(3);

FieldBuilder rightExpression = new FieldBuilder(FieldType.FieldFormula);
rightExpression.AddArgument(2.5);
rightExpression.AddArgument("*");
rightExpression.AddArgument(5.2);

// Als Nächstes erstellen wir zwei Feldargumente, die als Wahr/Falsch-Ausgabezeichenfolgen für das IF-Feld dienen.
// Diese Argumente verwenden die Ausgabewerte unserer numerischen Ausdrücke wieder.
FieldArgumentBuilder trueOutput = new FieldArgumentBuilder();
trueOutput.AddText("True, both expressions amount to ");
trueOutput.AddField(leftExpression);

FieldArgumentBuilder falseOutput = new FieldArgumentBuilder();
falseOutput.AddNode(new Run(doc, "False, "));
falseOutput.AddField(leftExpression);
falseOutput.AddNode(new Run(doc, " does not equal "));
falseOutput.AddField(rightExpression);

    // Abschließend erstellen wir noch einen Feldgenerator für das WENN-Feld und kombinieren alle Ausdrücke.
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

* class [FieldArgumentBuilder](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
