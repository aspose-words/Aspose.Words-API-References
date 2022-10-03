---
title: FieldBuilder
second_title: Aspose.Words per .NET API Reference
description: Crea un campo dai token del codice campo argomenti e opzioni.
type: docs
weight: 1510
url: /it/net/aspose.words.fields/fieldbuilder/
---
## FieldBuilder class

Crea un campo dai token del codice campo (argomenti e opzioni).

```csharp
public class FieldBuilder
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [FieldBuilder](fieldbuilder/)(FieldType) | Inizializza un'istanza di[`FieldBuilder`](./fieldbuilder/) classe. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [AddArgument](../../aspose.words.fields/fieldbuilder/addargument/#addargument_2)(double) | Aggiunge l'argomento di un campo. |
| [AddArgument](../../aspose.words.fields/fieldbuilder/addargument/#addargument)(FieldArgumentBuilder) | Aggiunge l'argomento di un campo rappresentato da[`FieldArgumentBuilder`](../fieldargumentbuilder/) al codice del campo. |
| [AddArgument](../../aspose.words.fields/fieldbuilder/addargument/#addargument_1)(FieldBuilder) | Aggiunge un campo figlio rappresentato da un altro[`FieldBuilder`](./fieldbuilder/) al codice del campo. |
| [AddArgument](../../aspose.words.fields/fieldbuilder/addargument/#addargument_3)(int) | Aggiunge l'argomento di un campo. |
| [AddArgument](../../aspose.words.fields/fieldbuilder/addargument/#addargument_4)(string) | Aggiunge l'argomento di un campo. |
| [AddSwitch](../../aspose.words.fields/fieldbuilder/addswitch/#addswitch)(string) | Aggiunge l'opzione di un campo. |
| [AddSwitch](../../aspose.words.fields/fieldbuilder/addswitch/#addswitch_1)(string, double) | Aggiunge l'opzione di un campo. |
| [AddSwitch](../../aspose.words.fields/fieldbuilder/addswitch/#addswitch_2)(string, int) | Aggiunge l'opzione di un campo. |
| [AddSwitch](../../aspose.words.fields/fieldbuilder/addswitch/#addswitch_3)(string, string) | Aggiunge l'opzione di un campo. |
| [BuildAndInsert](../../aspose.words.fields/fieldbuilder/buildandinsert/#buildandinsert)(Inline) | Crea e inserisce un campo nel documento prima del nodo inline specificato. |
| [BuildAndInsert](../../aspose.words.fields/fieldbuilder/buildandinsert/#buildandinsert_1)(Paragraph) | Crea e inserisce un campo nel documento fino alla fine del paragrafo specificato. |

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

* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields/)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
