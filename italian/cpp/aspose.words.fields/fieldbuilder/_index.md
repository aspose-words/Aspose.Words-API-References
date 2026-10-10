---
title: "Aspose::Words::Fields::FieldBuilder classe"
linktitle: "FieldBuilder"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldBuilder classe. Crea un campo dai token del codice del campo (argomenti e opzioni). Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 20000
url: /it/cpp/aspose.words.fields/fieldbuilder/
---
## FieldBuilder class


Crea un campo a partire dai token del codice del campo (argomenti e opzioni). Per saperne di più, visita l'articolo di documentazione [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldBuilder : public Aspose::Words::Fields::IFieldBuildingBlock
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [AddArgument](./addargument/)(const System::String\&) | Aggiunge un argomento al campo. |
| [AddArgument](./addargument/)(int32_t) | Aggiunge un argomento al campo. |
| [AddArgument](./addargument/)(double) | Aggiunge un argomento al campo. |
| [AddArgument](./addargument/)(const System::SharedPtr\<Aspose::Words::Fields::FieldBuilder\>\&) | Aggiunge un campo figlio rappresentato da un altro [FieldBuilder](./) al codice del campo. |
| [AddArgument](./addargument/)(const System::SharedPtr\<Aspose::Words::Fields::FieldArgumentBuilder\>\&) | Aggiunge un argomento al campo rappresentato da [FieldArgumentBuilder](../fieldargumentbuilder/) al codice del campo. |
| [AddSwitch](./addswitch/)(const System::String\&) | Aggiunge un'opzione al campo. |
| [AddSwitch](./addswitch/)(const System::String\&, const System::String\&) | Aggiunge un'opzione al campo. |
| [AddSwitch](./addswitch/)(const System::String\&, int32_t) | Aggiunge un'opzione al campo. |
| [AddSwitch](./addswitch/)(const System::String\&, double) | Aggiunge un'opzione al campo. |
| [BuildAndInsert](./buildandinsert/)(const System::SharedPtr\<Aspose::Words::Inline\>\&) | Crea e inserisce un campo nel documento prima del nodo inline specificato. |
| [BuildAndInsert](./buildandinsert/)(const System::SharedPtr\<Aspose::Words::Paragraph\>\&) | Crea e inserisce un campo nel documento alla fine del paragrafo specificato. |
| [FieldBuilder](./fieldbuilder/)(Aspose::Words::Fields::FieldType) | Inizializza un'istanza della classe [FieldBuilder](./). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Esempi



Mostra come costruire campi usando un costruttore di campi, e poi inserirli nel documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Di seguito sono riportati tre esempi di costruzione di campi eseguiti usando un costruttore di campi.
// 1 -  Campo singolo:
// Utilizza un costruttore di campi per aggiungere un campo SYMBOL che visualizza il simbolo ƒ (Fiorino).
auto builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldSymbol);
builder->AddArgument(402);
builder->AddSwitch(u"\\f", u"Arial");
builder->AddSwitch(u"\\s", 25);
builder->AddSwitch(u"\\u");
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->get_FirstParagraph());

ASSERT_EQ(u" SYMBOL 402 \\f Arial \\s 25 \\u ", field->GetFieldCode());

// 2 -  Campo annidato:
// Utilizza un costruttore di campi per creare un campo formula utilizzato come campo interno da un altro costruttore di campi.
auto innerFormulaBuilder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
innerFormulaBuilder->AddArgument(100);
innerFormulaBuilder->AddArgument(u"+");
innerFormulaBuilder->AddArgument(74);

// Crea un altro costruttore per un altro campo SYMBOL e inserisci il campo formula
// che abbiamo creato sopra nel campo SYMBOL come suo argomento.
builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldSymbol);
builder->AddArgument(innerFormulaBuilder);
field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->AppendParagraph(System::String::Empty));

// Il campo SYMBOL esterno utilizzerà il risultato del campo formula, 174, come suo argomento,
// il che farà visualizzare al campo il simbolo ® (Segno di registrazione) poiché il suo numero di carattere è 174.
ASSERT_EQ(u" SYMBOL \u0013 = 100 + 74 \u0014\u0015 ", field->GetFieldCode());

// 3 -  Molteplici campi annidati e argomenti:
// Ora, utilizzeremo un costruttore per creare un campo IF, che visualizza uno dei due valori stringa personalizzati,
// a seconda del valore vero/falso della sua espressione. Per ottenere un valore vero/falso
// che determina quale stringa visualizza il campo IF, il campo IF testerà due espressioni numeriche per uguaglianza.
// Forniremo le due espressioni sotto forma di campi formula, che annideremo all'interno del campo IF.
auto leftExpression = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
leftExpression->AddArgument(2);
leftExpression->AddArgument(u"+");
leftExpression->AddArgument(3);

auto rightExpression = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
rightExpression->AddArgument(2.5);
rightExpression->AddArgument(u"*");
rightExpression->AddArgument(5.2);

// Successivamente, costruiremo due argomenti di campo, che serviranno come stringhe di output vero/falso per il campo IF.
// Questi argomenti riutilizzeranno i valori di output delle nostre espressioni numeriche.
auto trueOutput = System::MakeObject<Aspose::Words::Fields::FieldArgumentBuilder>();
trueOutput->AddText(u"True, both expressions amount to ");
trueOutput->AddField(leftExpression);

auto falseOutput = System::MakeObject<Aspose::Words::Fields::FieldArgumentBuilder>();
falseOutput->AddNode(System::MakeObject<Aspose::Words::Run>(doc, u"False, "));
falseOutput->AddField(leftExpression);
falseOutput->AddNode(System::MakeObject<Aspose::Words::Run>(doc, u" does not equal "));
falseOutput->AddField(rightExpression);

// Infine, creeremo un altro costruttore di campi per il campo IF e combineremo tutte le espressioni.
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

## Vedi anche

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
