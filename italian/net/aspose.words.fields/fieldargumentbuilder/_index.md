---
title: FieldArgumentBuilder Class
linktitle: FieldArgumentBuilder
articleTitle: FieldArgumentBuilder
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Fields.FieldArgumentBuilder per creare senza sforzo argomenti di campo complessi con nodi e testo per una migliore automazione dei documenti.
type: docs
weight: 1960
url: /it/net/aspose.words.fields/fieldargumentbuilder/
---
## FieldArgumentBuilder class

Crea un argomento di campo complesso costituito da campi, nodi e testo normale.

Per saperne di più, visita il[Lavorare con i campi](https://docs.aspose.com/words/net/working-with-fields/) articolo di documentazione.

```csharp
public class FieldArgumentBuilder
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [FieldArgumentBuilder](fieldargumentbuilder/)() | Inizializza un'istanza di`FieldArgumentBuilder` classe. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [AddField](../../aspose.words.fields/fieldargumentbuilder/addfield/)(*[FieldBuilder](../fieldbuilder/)*) | Aggiunge un campo rappresentato da un[`FieldBuilder`](../fieldbuilder/) all'argomento. |
| [AddNode](../../aspose.words.fields/fieldargumentbuilder/addnode/)(*[Inline](../../aspose.words/inline/)*) | Aggiunge un nodo all'argomento. |
| [AddText](../../aspose.words.fields/fieldargumentbuilder/addtext/)(*string*) | Aggiunge un testo normale all'argomento. |

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

* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields/)
* assemblea [Aspose.Words](../../)
