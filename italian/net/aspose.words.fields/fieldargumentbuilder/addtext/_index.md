---
title: FieldArgumentBuilder.AddText
linktitle: AddText
articleTitle: AddText
second_title: Aspose.Words per .NET
description: Migliora i tuoi argomenti con il metodo AddText di FieldArgumentBuilder. Aggiungi facilmente testo semplice per maggiore chiarezza e funzionalità.
type: docs
weight: 40
url: /it/net/aspose.words.fields/fieldargumentbuilder/addtext/
---
## FieldArgumentBuilder.AddText method

Aggiunge un testo normale all'argomento.

```csharp
public FieldArgumentBuilder AddText(string text)
```

## Esempi

Mostra come creare campi utilizzando un generatore di campi e poi inserirli nel documento.

```csharp
Document doc = new Document();

// Di seguito sono riportati tre esempi di costruzione di campi realizzati utilizzando un generatore di campi.
// 1 - Campo singolo:
// Utilizzare un generatore di campi per aggiungere un campo SIMBOLO che visualizzi il simbolo ƒ (Fiordino).
FieldBuilder builder = new FieldBuilder(FieldType.FieldSymbol);
builder.AddArgument(402);
builder.AddSwitch("\\f", "Arial");
builder.AddSwitch("\\s", 25);
builder.AddSwitch("\\u");
Field field = builder.BuildAndInsert(doc.FirstSection.Body.FirstParagraph);

Assert.AreEqual(" SYMBOL 402 \\f Arial \\s 25 \\u ", field.GetFieldCode());

// 2 - Campo annidato:
// Utilizzare un generatore di campi per creare un campo formula utilizzato come campo interno da un altro generatore di campi.
FieldBuilder innerFormulaBuilder = new FieldBuilder(FieldType.FieldFormula);
innerFormulaBuilder.AddArgument(100);
innerFormulaBuilder.AddArgument("+");
innerFormulaBuilder.AddArgument(74);

// Crea un altro costruttore per un altro campo SIMBOLO e inserisci il campo formula
 // che abbiamo creato sopra nel campo SYMBOL come argomento.
builder = new FieldBuilder(FieldType.FieldSymbol);
builder.AddArgument(innerFormulaBuilder);
field = builder.BuildAndInsert(doc.FirstSection.Body.AppendParagraph(string.Empty));

// Il campo SIMBOLO esterno utilizzerà il risultato del campo formula, 174, come argomento,
// che farà sì che il campo visualizzi il simbolo ® (simbolo registrato) poiché il suo numero di carattere è 174.
Assert.AreEqual(" SYMBOL \u0013 = 100 + 74 \u0014\u0015 ", field.GetFieldCode());

// 3 - Più campi e argomenti annidati:
// Ora, useremo un builder per creare un campo IF, che visualizza uno dei due valori stringa personalizzati,
// a seconda del valore vero/falso della sua espressione. Per ottenere un valore vero/falso
// che determina quale stringa viene visualizzata nel campo SE; il campo SE verificherà l'uguaglianza di due espressioni numeriche.
// Forniremo le due espressioni sotto forma di campi formula, che annideremo all'interno del campo SE.
FieldBuilder leftExpression = new FieldBuilder(FieldType.FieldFormula);
leftExpression.AddArgument(2);
leftExpression.AddArgument("+");
leftExpression.AddArgument(3);

FieldBuilder rightExpression = new FieldBuilder(FieldType.FieldFormula);
rightExpression.AddArgument(2.5);
rightExpression.AddArgument("*");
rightExpression.AddArgument(5.2);

// Successivamente, creeremo due argomenti di campo, che fungeranno da stringhe di output true/false per il campo IF.
// Questi argomenti riutilizzeranno i valori di output delle nostre espressioni numeriche.
FieldArgumentBuilder trueOutput = new FieldArgumentBuilder();
trueOutput.AddText("True, both expressions amount to ");
trueOutput.AddField(leftExpression);

FieldArgumentBuilder falseOutput = new FieldArgumentBuilder();
falseOutput.AddNode(new Run(doc, "False, "));
falseOutput.AddField(leftExpression);
falseOutput.AddNode(new Run(doc, " does not equal "));
falseOutput.AddField(rightExpression);

 // Infine, creeremo un altro generatore di campi per il campo SE e combineremo tutte le espressioni.
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

* class [FieldArgumentBuilder](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
