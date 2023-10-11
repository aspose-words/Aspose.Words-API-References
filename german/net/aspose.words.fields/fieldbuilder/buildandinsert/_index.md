---
title: FieldBuilder.BuildAndInsert
second_title: Aspose.Words für .NET-API-Referenz
description: FieldBuilder methode. Erstellt ein Feld und fügt es vor dem angegebenen InlineKnoten in das Dokument ein.
type: docs
weight: 40
url: /de/net/aspose.words.fields/fieldbuilder/buildandinsert/
---
## BuildAndInsert(Inline) {#buildandinsert}

Erstellt ein Feld und fügt es vor dem angegebenen Inline-Knoten in das Dokument ein.

```csharp
public Field BuildAndInsert(Inline refNode)
```

### Rückgabewert

A[`Field`](../../field/) Objekt, das das eingefügte Feld darstellt.

### Beispiele

Zeigt, wie man ein Feld mit einem Feld-Builder erstellt und einfügt.

```csharp
Document doc = new Document();

// Eine bequeme Möglichkeit, Textinhalte zu einem Dokument hinzuzufügen, ist die Verwendung eines Document Builders.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write(" Hello world! This text is one Run, which is an inline node.");

// Felder haben ihren Builder, mit dem wir Stück für Stück einen Feldcode erstellen können.
// In diesem Fall erstellen wir ein BARCODE-Feld, das eine US-Postleitzahl darstellt.
// und dann vor einem Run einfügen.
FieldBuilder fieldBuilder = new FieldBuilder(FieldType.FieldBarcode);
fieldBuilder.AddArgument("90210");
fieldBuilder.AddSwitch("\\f", "A");
fieldBuilder.AddSwitch("\\u");

fieldBuilder.BuildAndInsert(doc.FirstSection.Body.FirstParagraph.Runs[0]);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CreateWithFieldBuilder.docx");
```

### Siehe auch

* class [Field](../../field/)
* class [Inline](../../../aspose.words/inline/)
* class [FieldBuilder](../)
* namensraum [Aspose.Words.Fields](../../fieldbuilder/)
* Montage [Aspose.Words](../../../)

---

## BuildAndInsert(Paragraph) {#buildandinsert_1}

Erstellt ein Feld und fügt es bis zum Ende des angegebenen Absatzes in das Dokument ein.

```csharp
public Field BuildAndInsert(Paragraph refNode)
```

### Rückgabewert

A[`Field`](../../field/) Objekt, das das eingefügte Feld darstellt.

### Beispiele

Zeigt, wie Felder mit einem Feld-Builder erstellt und dann in das Dokument eingefügt werden.

```csharp
Document doc = new Document();

// Nachfolgend finden Sie drei Beispiele für die Feldkonstruktion, die mit einem Feld-Builder durchgeführt wurde.
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
// Verwenden Sie einen Feld-Builder, um ein Formelfeld zu erstellen, das von einem anderen Feld-Builder als inneres Feld verwendet wird.
FieldBuilder innerFormulaBuilder = new FieldBuilder(FieldType.FieldFormula);
innerFormulaBuilder.AddArgument(100);
innerFormulaBuilder.AddArgument("+");
innerFormulaBuilder.AddArgument(74);

// Einen weiteren Builder für ein anderes SYMBOL-Feld erstellen und das Formelfeld einfügen
 // das wir oben erstellt haben, als Argument in das SYMBOL-Feld ein.
builder = new FieldBuilder(FieldType.FieldSymbol);
builder.AddArgument(innerFormulaBuilder);
field = builder.BuildAndInsert(doc.FirstSection.Body.AppendParagraph(string.Empty));

// Das äußere SYMBOL-Feld verwendet das Formelfeldergebnis 174 als Argument.
// wodurch das Feld das Symbol ® (Registered Sign) anzeigt, da seine Zeichennummer 174 ist.
Assert.AreEqual(" SYMBOL \u0013 = 100 + 74 \u0014\u0015 ", field.GetFieldCode());

// 3 – Mehrere verschachtelte Felder und Argumente:
// Jetzt verwenden wir einen Builder, um ein IF-Feld zu erstellen, das einen von zwei benutzerdefinierten Zeichenfolgenwerten anzeigt.
// abhängig vom wahren/falschen Wert seines Ausdrucks. Um einen wahren/falschen Wert zu erhalten
// das bestimmt, welche Zeichenfolge das IF-Feld anzeigt. Das IF-Feld prüft zwei numerische Ausdrücke auf Gleichheit.
// Wir stellen die beiden Ausdrücke in Form von Formelfeldern bereit, die wir im IF-Feld verschachteln.
FieldBuilder leftExpression = new FieldBuilder(FieldType.FieldFormula);
leftExpression.AddArgument(2);
leftExpression.AddArgument("+");
leftExpression.AddArgument(3);

FieldBuilder rightExpression = new FieldBuilder(FieldType.FieldFormula);
rightExpression.AddArgument(2.5);
rightExpression.AddArgument("*");
rightExpression.AddArgument(5.2);

// Als nächstes erstellen wir zwei Feldargumente, die als True/False-Ausgabezeichenfolgen für das IF-Feld dienen.
// Diese Argumente verwenden die Ausgabewerte unserer numerischen Ausdrücke wieder.
FieldArgumentBuilder trueOutput = new FieldArgumentBuilder();
trueOutput.AddText("True, both expressions amount to ");
trueOutput.AddField(leftExpression);

FieldArgumentBuilder falseOutput = new FieldArgumentBuilder();
falseOutput.AddNode(new Run(doc, "False, "));
falseOutput.AddField(leftExpression);
falseOutput.AddNode(new Run(doc, " does not equal "));
falseOutput.AddField(rightExpression);

 // Abschließend erstellen wir einen weiteren Feldgenerator für das IF-Feld und kombinieren alle Ausdrücke.
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

* class [Field](../../field/)
* class [Paragraph](../../../aspose.words/paragraph/)
* class [FieldBuilder](../)
* namensraum [Aspose.Words.Fields](../../fieldbuilder/)
* Montage [Aspose.Words](../../../)


