---
title: FieldArgumentBuilder.AddText
linktitle: AddText
articleTitle: AddText
second_title: Aspose.Words för .NET
description: Förbättra dina argument med FieldArgumentBuilder AddText-metoden. Lägg enkelt till vanlig text för förbättrad tydlighet och funktionalitet.
type: docs
weight: 40
url: /sv/net/aspose.words.fields/fieldargumentbuilder/addtext/
---
## FieldArgumentBuilder.AddText method

Lägger till vanlig text i argumentet.

```csharp
public FieldArgumentBuilder AddText(string text)
```

## Exempel

Visar hur man konstruerar fält med hjälp av en fältbyggare och sedan infogar dem i dokumentet.

```csharp
Document doc = new Document();

// Nedan följer tre exempel på fältkonstruktion gjord med en fältbyggare.
// 1 - Enskilt fält:
// Använd en fältbyggare för att lägga till ett SYMBOL-fält som visar symbolen ƒ (Florin).
FieldBuilder builder = new FieldBuilder(FieldType.FieldSymbol);
builder.AddArgument(402);
builder.AddSwitch("\\f", "Arial");
builder.AddSwitch("\\s", 25);
builder.AddSwitch("\\u");
Field field = builder.BuildAndInsert(doc.FirstSection.Body.FirstParagraph);

Assert.AreEqual(" SYMBOL 402 \\f Arial \\s 25 \\u ", field.GetFieldCode());

// 2 - Kapslat fält:
// Använd en fältbyggare för att skapa ett formelfält som används som ett inre fält av en annan fältbyggare.
FieldBuilder innerFormulaBuilder = new FieldBuilder(FieldType.FieldFormula);
innerFormulaBuilder.AddArgument(100);
innerFormulaBuilder.AddArgument("+");
innerFormulaBuilder.AddArgument(74);

// Skapa en annan verktygsbyggare för ett annat SYMBOL-fält och infoga formelfältet
 // som vi har skapat ovan i SYMBOL-fältet som dess argument.
builder = new FieldBuilder(FieldType.FieldSymbol);
builder.AddArgument(innerFormulaBuilder);
field = builder.BuildAndInsert(doc.FirstSection.Body.AppendParagraph(string.Empty));

// Det yttre SYMBOL-fältet kommer att använda formelfältets resultat, 174, som sitt argument,
// vilket gör att fältet visar symbolen ® (registrerat tecken) eftersom dess teckennummer är 174.
Assert.AreEqual(" SYMBOL \u0013 = 100 + 74 \u0014\u0015 ", field.GetFieldCode());

// 3 - Flera kapslade fält och argument:
// Nu ska vi använda en byggare för att skapa ett OM-fält, som visar ett av två anpassade strängvärden,
// beroende på det sanna/falska värdet i dess uttryck. För att få ett sant/falskt värde
// som avgör vilken sträng OM-fältet visar, OM-fältet kommer att testa två numeriska uttryck för likhet.
// Vi kommer att tillhandahålla de två uttrycken i form av formelfält, som vi kommer att kapsla inuti OM-fältet.
FieldBuilder leftExpression = new FieldBuilder(FieldType.FieldFormula);
leftExpression.AddArgument(2);
leftExpression.AddArgument("+");
leftExpression.AddArgument(3);

FieldBuilder rightExpression = new FieldBuilder(FieldType.FieldFormula);
rightExpression.AddArgument(2.5);
rightExpression.AddArgument("*");
rightExpression.AddArgument(5.2);

// Härnäst ska vi bygga två fältargument, som kommer att fungera som sant/falskt utdatasträngar för OM-fältet.
// Dessa argument kommer att återanvända utdatavärdena från våra numeriska uttryck.
FieldArgumentBuilder trueOutput = new FieldArgumentBuilder();
trueOutput.AddText("True, both expressions amount to ");
trueOutput.AddField(leftExpression);

FieldArgumentBuilder falseOutput = new FieldArgumentBuilder();
falseOutput.AddNode(new Run(doc, "False, "));
falseOutput.AddField(leftExpression);
falseOutput.AddNode(new Run(doc, " does not equal "));
falseOutput.AddField(rightExpression);

 // Slutligen skapar vi ytterligare en fältbyggare för OM-fältet och kombinerar alla uttryck.
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

### Se även

* class [FieldArgumentBuilder](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
