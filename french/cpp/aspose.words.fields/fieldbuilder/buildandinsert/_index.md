---
title: "Aspose::Words::Fields::FieldBuilder::BuildAndInsert méthode"
linktitle: "BuildAndInsert"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldBuilder::BuildAndInsert méthode. Construit et insère un champ dans le document avant le nœud en ligne spécifié en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.fields/fieldbuilder/buildandinsert/
---
## FieldBuilder::BuildAndInsert(const System::SharedPtr\<Aspose::Words::Inline\>\&) method


Construit et insère un champ dans le document avant le nœud en ligne spécifié.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Fields::FieldBuilder::BuildAndInsert(const System::SharedPtr<Aspose::Words::Inline> &refNode)
```


### ReturnValue

Un objet [Field](../../field/) qui représente le champ inséré.

## Exemples



Montre comment créer et insérer un champ à l'aide d'un constructeur de champ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Une façon pratique d'ajouter du texte à un document est d'utiliser un constructeur de document.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u" Hello world! This text is one Run, which is an inline node.");

// Les champs ont leur constructeur, que nous pouvons utiliser pour construire le code d'un champ morceau par morceau.
// Dans ce cas, nous allons construire un champ BARCODE représentant un code postal US,
// et puis l'insérer devant un Run.
auto fieldBuilder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldBarcode);
fieldBuilder->AddArgument(u"90210");
fieldBuilder->AddSwitch(u"\\f", u"A");
fieldBuilder->AddSwitch(u"\\u");

fieldBuilder->BuildAndInsert(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0));

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.CreateWithFieldBuilder.docx");
```

## Voir aussi

* Class [Field](../../field/)
* Class [Inline](../../../aspose.words/inline/)
* Class [FieldBuilder](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
## FieldBuilder::BuildAndInsert(const System::SharedPtr\<Aspose::Words::Paragraph\>\&) method


Construit et insère un champ dans le document à la fin du paragraphe spécifié.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Fields::FieldBuilder::BuildAndInsert(const System::SharedPtr<Aspose::Words::Paragraph> &refNode)
```


### ReturnValue

Un objet [Field](../../field/) qui représente le champ inséré.

## Exemples



Montre comment construire des champs à l'aide d'un constructeur de champs, puis les insérer dans le document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Ci-dessous trois exemples de construction de champs réalisés à l'aide d'un constructeur de champs.
// 1 -  Champ unique:
// Utilisez un constructeur de champ pour ajouter un champ SYMBOL qui affiche le symbole ƒ (Florin).
auto builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldSymbol);
builder->AddArgument(402);
builder->AddSwitch(u"\\f", u"Arial");
builder->AddSwitch(u"\\s", 25);
builder->AddSwitch(u"\\u");
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->get_FirstParagraph());

ASSERT_EQ(u" SYMBOL 402 \\f Arial \\s 25 \\u ", field->GetFieldCode());

// 2 -  Champ imbriqué:
// Utilisez un constructeur de champ pour créer un champ de formule utilisé comme champ interne par un autre constructeur de champ.
auto innerFormulaBuilder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
innerFormulaBuilder->AddArgument(100);
innerFormulaBuilder->AddArgument(u"+");
innerFormulaBuilder->AddArgument(74);

// Créez un autre constructeur pour un autre champ SYMBOL, et insérez le champ de formule
// que nous avons créé ci-dessus dans le champ SYMBOL comme argument.
builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldSymbol);
builder->AddArgument(innerFormulaBuilder);
field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->AppendParagraph(System::String::Empty));

// Le champ SYMBOL externe utilisera le résultat du champ de formule, 174, comme argument,
// ce qui fera afficher au champ le symbole ® (signe d'enregistrement) puisque son numéro de caractère est 174.
ASSERT_EQ(u" SYMBOL \u0013 = 100 + 74 \u0014\u0015 ", field->GetFieldCode());

// 3 -  Plusieurs champs imbriqués et arguments:
// Maintenant, nous utiliserons un constructeur pour créer un champ IF, qui affiche l'une des deux valeurs de chaîne personnalisées,
// en fonction de la valeur vrai/faux de son expression. Pour obtenir une valeur vrai/faux
// qui détermine quelle chaîne le champ IF affiche, le champ IF testera l'égalité de deux expressions numériques.
// Nous fournirons les deux expressions sous forme de champs de formule, que nous imbriquerons à l'intérieur du champ IF.
auto leftExpression = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
leftExpression->AddArgument(2);
leftExpression->AddArgument(u"+");
leftExpression->AddArgument(3);

auto rightExpression = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
rightExpression->AddArgument(2.5);
rightExpression->AddArgument(u"*");
rightExpression->AddArgument(5.2);

// Ensuite, nous construirons deux arguments de champ, qui serviront de chaînes de sortie vrai/faux pour le champ IF.
// Ces arguments réutiliseront les valeurs de sortie de nos expressions numériques.
auto trueOutput = System::MakeObject<Aspose::Words::Fields::FieldArgumentBuilder>();
trueOutput->AddText(u"True, both expressions amount to ");
trueOutput->AddField(leftExpression);

auto falseOutput = System::MakeObject<Aspose::Words::Fields::FieldArgumentBuilder>();
falseOutput->AddNode(System::MakeObject<Aspose::Words::Run>(doc, u"False, "));
falseOutput->AddField(leftExpression);
falseOutput->AddNode(System::MakeObject<Aspose::Words::Run>(doc, u" does not equal "));
falseOutput->AddField(rightExpression);

// Enfin, nous créerons un autre constructeur de champ pour le champ IF et combinerons toutes les expressions.
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

## Voir aussi

* Class [Field](../../field/)
* Class [Paragraph](../../../aspose.words/paragraph/)
* Class [FieldBuilder](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
