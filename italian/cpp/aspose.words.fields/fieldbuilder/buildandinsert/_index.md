---
title: "Aspose::Words::Fields::FieldBuilder::BuildAndInsert metodo"
linktitle: "BuildAndInsert"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldBuilder::BuildAndInsert metodo. Costruisce e inserisce un campo nel documento prima del nodo inline specificato in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.fields/fieldbuilder/buildandinsert/
---
## FieldBuilder::BuildAndInsert(const System::SharedPtr\<Aspose::Words::Inline\>\&) method


Crea e inserisce un campo nel documento prima del nodo inline specificato.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Fields::FieldBuilder::BuildAndInsert(const System::SharedPtr<Aspose::Words::Inline> &refNode)
```


### ReturnValue

Un oggetto [Field](../../field/) che rappresenta il campo inserito.

## Esempi



Mostra come creare e inserire un campo utilizzando un field builder.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Un modo comodo per aggiungere contenuto testuale a un documento è con un document builder.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u" Hello world! This text is one Run, which is an inline node.");

// I campi hanno il loro builder, che possiamo usare per costruire il codice del campo pezzo per pezzo.
// In questo caso, costruiremo un campo BARCODE che rappresenta un codice postale statunitense,
// e poi lo inseriremo davanti a un Run.
auto fieldBuilder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldBarcode);
fieldBuilder->AddArgument(u"90210");
fieldBuilder->AddSwitch(u"\\f", u"A");
fieldBuilder->AddSwitch(u"\\u");

fieldBuilder->BuildAndInsert(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0));

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.CreateWithFieldBuilder.docx");
```

## Vedi anche

* Class [Field](../../field/)
* Class [Inline](../../../aspose.words/inline/)
* Class [FieldBuilder](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
## FieldBuilder::BuildAndInsert(const System::SharedPtr\<Aspose::Words::Paragraph\>\&) method


Crea e inserisce un campo nel documento alla fine del paragrafo specificato.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Fields::FieldBuilder::BuildAndInsert(const System::SharedPtr<Aspose::Words::Paragraph> &refNode)
```


### ReturnValue

Un oggetto [Field](../../field/) che rappresenta il campo inserito.

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

* Class [Field](../../field/)
* Class [Paragraph](../../../aspose.words/paragraph/)
* Class [FieldBuilder](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
