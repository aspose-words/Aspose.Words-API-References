---
title: "Aspose::Words::Fields::FieldBuilder klass"
linktitle: "FieldBuilder"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldBuilder klass. Bygger ett fält från fältkodstoken (argument och växlar). För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 20000
url: /sv/cpp/aspose.words.fields/fieldbuilder/
---
## FieldBuilder class


Skapar ett fält från fältkodstoken (argument och växlar). För att lära dig mer, besök [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) dokumentationsartikel.

```cpp
class FieldBuilder : public Aspose::Words::Fields::IFieldBuildingBlock
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [AddArgument](./addargument/)(const System::String\&) | Lägger till ett fälts argument. |
| [AddArgument](./addargument/)(int32_t) | Lägger till ett fälts argument. |
| [AddArgument](./addargument/)(double) | Lägger till ett fälts argument. |
| [AddArgument](./addargument/)(const System::SharedPtr\<Aspose::Words::Fields::FieldBuilder\>\&) | Lägger till ett underfält som representeras av en annan [FieldBuilder](./) till fältets kod. |
| [AddArgument](./addargument/)(const System::SharedPtr\<Aspose::Words::Fields::FieldArgumentBuilder\>\&) | Lägger till ett fälts argument som representeras av [FieldArgumentBuilder](../fieldargumentbuilder/) till fältets kod. |
| [AddSwitch](./addswitch/)(const System::String\&) | Lägger till ett fälts växel. |
| [AddSwitch](./addswitch/)(const System::String\&, const System::String\&) | Lägger till ett fälts växel. |
| [AddSwitch](./addswitch/)(const System::String\&, int32_t) | Lägger till ett fälts växel. |
| [AddSwitch](./addswitch/)(const System::String\&, double) | Lägger till ett fälts växel. |
| [BuildAndInsert](./buildandinsert/)(const System::SharedPtr\<Aspose::Words::Inline\>\&) | Bygger och infogar ett fält i dokumentet före den specificerade inline‑noden. |
| [BuildAndInsert](./buildandinsert/)(const System::SharedPtr\<Aspose::Words::Paragraph\>\&) | Bygger och infogar ett fält i dokumentet till slutet av det specificerade stycket. |
| [FieldBuilder](./fieldbuilder/)(Aspose::Words::Fields::FieldType) | Initierar en instans av [FieldBuilder](./) klass. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Exempel



Visar hur man konstruerar fält med en fältbyggare och sedan infogar dem i dokumentet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Nedan följer tre exempel på fältkonstruktion med en fältbyggare.
// 1 -  Enkelt fält:
// Använd en fältbyggare för att lägga till ett SYMBOL-fält som visar tecknet ƒ (Florin).
auto builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldSymbol);
builder->AddArgument(402);
builder->AddSwitch(u"\\f", u"Arial");
builder->AddSwitch(u"\\s", 25);
builder->AddSwitch(u"\\u");
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->get_FirstParagraph());

ASSERT_EQ(u" SYMBOL 402 \\f Arial \\s 25 \\u ", field->GetFieldCode());

// 2 -  Inbäddat fält:
// Använd en fältbyggare för att skapa ett formelfält som används som ett inre fält av en annan fältbyggare.
auto innerFormulaBuilder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
innerFormulaBuilder->AddArgument(100);
innerFormulaBuilder->AddArgument(u"+");
innerFormulaBuilder->AddArgument(74);

// Skapa en annan byggare för ett annat SYMBOL-fält och infoga formelfältet
// som vi har skapat ovan i SYMBOL-fältet som dess argument.
builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldSymbol);
builder->AddArgument(innerFormulaBuilder);
field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->AppendParagraph(System::String::Empty));

// Det yttre SYMBOL-fältet kommer att använda formelfältets resultat, 174, som dess argument,
// vilket får fältet att visa ® (Registrerad varumärkessymbol) eftersom dess teckennummer är 174.
ASSERT_EQ(u" SYMBOL \u0013 = 100 + 74 \u0014\u0015 ", field->GetFieldCode());

// 3 -  Flera inbäddade fält och argument:
// Nu kommer vi att använda en byggare för att skapa ett IF-fält som visar ett av två anpassade strängvärden,
// beroende på sant/falskt-värdet av dess uttryck. För att få ett sant/falskt-värde
// som bestämmer vilken sträng IF-fältet visar, kommer IF-fältet att testa två numeriska uttryck för likhet.
// Vi kommer att tillhandahålla de två uttrycken i form av formelfält, som vi kommer att bädda in i IF-fältet.
auto leftExpression = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
leftExpression->AddArgument(2);
leftExpression->AddArgument(u"+");
leftExpression->AddArgument(3);

auto rightExpression = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
rightExpression->AddArgument(2.5);
rightExpression->AddArgument(u"*");
rightExpression->AddArgument(5.2);

// Nästa steg är att bygga två fältargument som kommer att fungera som sant/falskt-utdatasträngar för IF-fältet.
// Dessa argument kommer att återanvända utdatavärdena från våra numeriska uttryck.
auto trueOutput = System::MakeObject<Aspose::Words::Fields::FieldArgumentBuilder>();
trueOutput->AddText(u"True, both expressions amount to ");
trueOutput->AddField(leftExpression);

auto falseOutput = System::MakeObject<Aspose::Words::Fields::FieldArgumentBuilder>();
falseOutput->AddNode(System::MakeObject<Aspose::Words::Run>(doc, u"False, "));
falseOutput->AddField(leftExpression);
falseOutput->AddNode(System::MakeObject<Aspose::Words::Run>(doc, u" does not equal "));
falseOutput->AddField(rightExpression);

// Slutligen kommer vi att skapa ytterligare en fältbyggare för IF-fältet och kombinera alla uttryck.
builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldIf);
builder->AddArgument(leftExpression);
builder->AddArgument(u"=");
builder->AddArgument(rightExpression);
builder->AddArgument(trueOutput);
builder->AddArgument(falseOutput);
field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->AppendParagraph(System::String::Empty));

ASSERT_EQ(System::String(u" IF \u0013 = 2 + 3 \u0014\u0015 = \u0013 = 2.5 * 5.2 \u0014\u0015 ") + u"\"True, both expressions amount to \u0013 = 2 + 3 \u0014\u0015\" " + u"\"False, \u0013 = 2 + 3 \u0014\u0015 does not equal \u0013 = 2.5 * 5.2 \u0014\u0015\" ", field->GetFieldCode());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SYMBOL.docx");
```

## Se även

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
