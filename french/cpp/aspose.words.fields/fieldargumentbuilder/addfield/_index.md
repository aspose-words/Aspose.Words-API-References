---
title: "Aspose::Words::Fields::FieldArgumentBuilder::AddField méthode"
linktitle: "AddField"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldArgumentBuilder::AddField méthode. Ajoute un champ représenté par un FieldBuilder à l'argument en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.fields/fieldargumentbuilder/addfield/
---
## FieldArgumentBuilder::AddField method


Ajoute un champ représenté par un [FieldBuilder](../../fieldbuilder/) à l'argument.

```cpp
System::SharedPtr<Aspose::Words::Fields::FieldArgumentBuilder> Aspose::Words::Fields::FieldArgumentBuilder::AddField(const System::SharedPtr<Aspose::Words::Fields::FieldBuilder> &fieldBuilder)
```


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

* Class [FieldArgumentBuilder](../)
* Class [FieldBuilder](../../fieldbuilder/)
* Class [FieldArgumentBuilder](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
