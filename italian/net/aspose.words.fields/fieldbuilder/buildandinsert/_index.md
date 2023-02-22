---
title: FieldBuilder.BuildAndInsert
second_title: Aspose.Words per .NET API Reference
description: FieldBuilder metodo. Crea e inserisce un campo nel documento prima del nodo inline specificato.
type: docs
weight: 40
url: /it/net/aspose.words.fields/fieldbuilder/buildandinsert/
---
## BuildAndInsert(Inline) {#buildandinsert}

Crea e inserisce un campo nel documento prima del nodo inline specificato.

```csharp
public Field BuildAndInsert(Inline refNode)
```

### Valore di ritorno

UN[`Field`](../../field/) oggetto che rappresenta il campo inserito.

### Esempi

Mostra come creare e inserire un campo utilizzando un generatore di campi.

```csharp
Document doc = new Document();

// Un modo conveniente per aggiungere contenuto di testo a un documento è con un generatore di documenti.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write(" Hello world! This text is one Run, which is an inline node.");

// I campi hanno il loro builder, che possiamo usare per costruire un codice di campo pezzo per pezzo.
// In questo caso, costruiremo un campo CODICE A BARRE che rappresenta un codice postale statunitense,
// e quindi inserirlo davanti a un Run.
FieldBuilder fieldBuilder = new FieldBuilder(FieldType.FieldBarcode);
fieldBuilder.AddArgument("90210");
fieldBuilder.AddSwitch("\\f", "A");
fieldBuilder.AddSwitch("\\u");

fieldBuilder.BuildAndInsert(doc.FirstSection.Body.FirstParagraph.Runs[0]);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CreateWithFieldBuilder.docx");
```

### Guarda anche

* class [Field](../../field/)
* class [Inline](../../../aspose.words/inline/)
* class [FieldBuilder](../)
* spazio dei nomi [Aspose.Words.Fields](../../fieldbuilder/)
* assemblea [Aspose.Words](../../../)

---

## BuildAndInsert(Paragraph) {#buildandinsert_1}

Crea e inserisce un campo nel documento fino alla fine del paragrafo specificato.

```csharp
public Field BuildAndInsert(Paragraph refNode)
```

### Valore di ritorno

UN[`Field`](../../field/) oggetto che rappresenta il campo inserito.

### Esempi

Mostra come costruire campi utilizzando un generatore di campi e quindi inserirli nel documento.

```csharp
Document doc = new Document();

// Di seguito sono riportati tre esempi di costruzione di campi eseguiti utilizzando un generatore di campi.
// 1 - Campo singolo:
// Usa un generatore di campi per aggiungere un campo SYMBOL che visualizzi il simbolo ƒ (Florin).
FieldBuilder builder = new FieldBuilder(FieldType.FieldSymbol);
builder.AddArgument(402);
builder.AddSwitch("\\f", "Arial");
builder.AddSwitch("\\s", 25);
builder.AddSwitch("\\u");
Field field = builder.BuildAndInsert(doc.FirstSection.Body.FirstParagraph);

Assert.AreEqual(" SYMBOL 402 \\f Arial \\s 25 \\u ", field.GetFieldCode());

// 2 - Campo nidificato:
// Utilizza un generatore di campi per creare un campo formula utilizzato come campo interno da un altro generatore di campi.
FieldBuilder innerFormulaBuilder = new FieldBuilder(FieldType.FieldFormula);
innerFormulaBuilder.AddArgument(100);
innerFormulaBuilder.AddArgument("+");
innerFormulaBuilder.AddArgument(74);

// Crea un altro builder per un altro campo SYMBOL e inserisci il campo formula
 // che abbiamo creato sopra nel campo SYMBOL come argomento.
builder = new FieldBuilder(FieldType.FieldSymbol);
builder.AddArgument(innerFormulaBuilder);
field = builder.BuildAndInsert(doc.FirstSection.Body.AppendParagraph(string.Empty));

// Il campo SYMBOL esterno utilizzerà il risultato del campo formula, 174, come argomento,
// che farà sì che il campo visualizzi il simbolo ® (segno registrato) poiché il suo numero di caratteri è 174.
Assert.AreEqual(" SYMBOL \u0013 = 100 + 74 \u0014\u0015 ", field.GetFieldCode());

// 3 - Più campi e argomenti nidificati:
// Ora useremo un builder per creare un campo IF, che mostra uno dei due valori di stringa personalizzati,
// a seconda del valore vero/falso della sua espressione. Per ottenere un valore vero/falso
// che determina quale stringa viene visualizzata dal campo SE, il campo SE verificherà l'uguaglianza di due espressioni numeriche.
// Forniremo le due espressioni sotto forma di campi formula, che annideremo all'interno del campo SE.
FieldBuilder leftExpression = new FieldBuilder(FieldType.FieldFormula);
leftExpression.AddArgument(2);
leftExpression.AddArgument("+");
leftExpression.AddArgument(3);

FieldBuilder rightExpression = new FieldBuilder(FieldType.FieldFormula);
rightExpression.AddArgument(2.5);
rightExpression.AddArgument("*");
rightExpression.AddArgument(5.2);

// Successivamente, creeremo due argomenti di campo, che fungeranno da stringhe di output vero/falso per il campo SE.
// Questi argomenti riutilizzeranno i valori di output delle nostre espressioni numeriche.
FieldArgumentBuilder trueOutput = new FieldArgumentBuilder();
trueOutput.AddText("True, both expressions amount to ");
trueOutput.AddField(leftExpression);

FieldArgumentBuilder falseOutput = new FieldArgumentBuilder();
falseOutput.AddNode(new Run(doc, "False, "));
falseOutput.AddField(leftExpression);
falseOutput.AddNode(new Run(doc, " does not equal "));
falseOutput.AddField(rightExpression);

 // Infine, creeremo un altro generatore di campi per il campo IF e combineremo tutte le espressioni.
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

### Guarda anche

* class [Field](../../field/)
* class [Paragraph](../../../aspose.words/paragraph/)
* class [FieldBuilder](../)
* spazio dei nomi [Aspose.Words.Fields](../../fieldbuilder/)
* assemblea [Aspose.Words](../../../)


