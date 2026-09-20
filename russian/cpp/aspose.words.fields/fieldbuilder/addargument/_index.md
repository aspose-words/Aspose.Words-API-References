---
title: "Метод Aspose::Words::Fields::FieldBuilder::AddArgument"
linktitle: "AddArgument"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Fields::FieldBuilder::AddArgument. Добавляет аргумент поля, представленный классом FieldArgumentBuilder, в код поля в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.fields/fieldbuilder/addargument/
---
## FieldBuilder::AddArgument(const System::SharedPtr\<Aspose::Words::Fields::FieldArgumentBuilder\>\&) method


Добавляет аргумент поля, представленный [FieldArgumentBuilder](../../fieldargumentbuilder/), в код поля.

```cpp
System::SharedPtr<Aspose::Words::Fields::FieldBuilder> Aspose::Words::Fields::FieldBuilder::AddArgument(const System::SharedPtr<Aspose::Words::Fields::FieldArgumentBuilder> &argument)
```


## Примеры



Показывает, как создавать поля с помощью построителя полей, а затем вставлять их в документ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Ниже приведены три примера построения полей с использованием построителя полей.
// 1 -  Одинарное поле:
// Используйте построитель полей, чтобы добавить поле SYMBOL, которое отображает символ ƒ (флорин).
auto builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldSymbol);
builder->AddArgument(402);
builder->AddSwitch(u"\\f", u"Arial");
builder->AddSwitch(u"\\s", 25);
builder->AddSwitch(u"\\u");
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->get_FirstParagraph());

ASSERT_EQ(u" SYMBOL 402 \\f Arial \\s 25 \\u ", field->GetFieldCode());

// 2 -  Вложенное поле:
// Используйте построитель полей, чтобы создать поле формулы, используемое как внутреннее поле другим построителем полей.
auto innerFormulaBuilder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
innerFormulaBuilder->AddArgument(100);
innerFormulaBuilder->AddArgument(u"+");
innerFormulaBuilder->AddArgument(74);

// Создайте еще один построитель для другого поля SYMBOL и вставьте поле формулы
// которое мы создали выше, в поле SYMBOL в качестве его аргумента.
builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldSymbol);
builder->AddArgument(innerFormulaBuilder);
field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->AppendParagraph(System::String::Empty));

// Внешнее поле SYMBOL будет использовать результат поля формулы, 174, в качестве своего аргумента,
// что заставит поле отображать символ ® (знак регистрации), поскольку его номер символа — 174.
ASSERT_EQ(u" SYMBOL \u0013 = 100 + 74 \u0014\u0015 ", field->GetFieldCode());

// 3 -  Несколько вложенных полей и аргументов:
// Теперь мы используем построитель, чтобы создать поле IF, которое отображает одну из двух пользовательских строковых значений,
// в зависимости от логического значения его выражения. Чтобы получить логическое значение
// которое определяет, какую строку отображает поле IF, поле IF проверит два числовых выражения на равенство.
// Мы предоставим два выражения в виде полей формулы, которые вложим внутрь поля IF.
auto leftExpression = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
leftExpression->AddArgument(2);
leftExpression->AddArgument(u"+");
leftExpression->AddArgument(3);

auto rightExpression = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
rightExpression->AddArgument(2.5);
rightExpression->AddArgument(u"*");
rightExpression->AddArgument(5.2);

// Затем мы создадим два аргумента поля, которые будут служить логическими (true/false) строками вывода для поля IF.
// Эти аргументы будут повторно использовать выходные значения наших числовых выражений.
auto trueOutput = System::MakeObject<Aspose::Words::Fields::FieldArgumentBuilder>();
trueOutput->AddText(u"True, both expressions amount to ");
trueOutput->AddField(leftExpression);

auto falseOutput = System::MakeObject<Aspose::Words::Fields::FieldArgumentBuilder>();
falseOutput->AddNode(System::MakeObject<Aspose::Words::Run>(doc, u"False, "));
falseOutput->AddField(leftExpression);
falseOutput->AddNode(System::MakeObject<Aspose::Words::Run>(doc, u" does not equal "));
falseOutput->AddField(rightExpression);

// Наконец, мы создадим еще один построитель полей для поля IF и объединим все выражения.
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

## См. также

* Class [FieldBuilder](../)
* Class [FieldArgumentBuilder](../../fieldargumentbuilder/)
* Class [FieldBuilder](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
## FieldBuilder::AddArgument(const System::SharedPtr\<Aspose::Words::Fields::FieldBuilder\>\&) method


Добавляет дочернее поле, представленный другим [FieldBuilder](../), в код поля.

```cpp
System::SharedPtr<Aspose::Words::Fields::FieldBuilder> Aspose::Words::Fields::FieldBuilder::AddArgument(const System::SharedPtr<Aspose::Words::Fields::FieldBuilder> &argument)
```


## Примеры



Показывает, как создавать поля с помощью построителя полей, а затем вставлять их в документ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Ниже приведены три примера построения полей с использованием построителя полей.
// 1 -  Одинарное поле:
// Используйте построитель полей, чтобы добавить поле SYMBOL, которое отображает символ ƒ (флорин).
auto builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldSymbol);
builder->AddArgument(402);
builder->AddSwitch(u"\\f", u"Arial");
builder->AddSwitch(u"\\s", 25);
builder->AddSwitch(u"\\u");
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->get_FirstParagraph());

ASSERT_EQ(u" SYMBOL 402 \\f Arial \\s 25 \\u ", field->GetFieldCode());

// 2 -  Вложенное поле:
// Используйте построитель полей, чтобы создать поле формулы, используемое как внутреннее поле другим построителем полей.
auto innerFormulaBuilder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
innerFormulaBuilder->AddArgument(100);
innerFormulaBuilder->AddArgument(u"+");
innerFormulaBuilder->AddArgument(74);

// Создайте еще один построитель для другого поля SYMBOL и вставьте поле формулы
// которое мы создали выше, в поле SYMBOL в качестве его аргумента.
builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldSymbol);
builder->AddArgument(innerFormulaBuilder);
field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->AppendParagraph(System::String::Empty));

// Внешнее поле SYMBOL будет использовать результат поля формулы, 174, в качестве своего аргумента,
// что заставит поле отображать символ ® (знак регистрации), поскольку его номер символа — 174.
ASSERT_EQ(u" SYMBOL \u0013 = 100 + 74 \u0014\u0015 ", field->GetFieldCode());

// 3 -  Несколько вложенных полей и аргументов:
// Теперь мы используем построитель, чтобы создать поле IF, которое отображает одну из двух пользовательских строковых значений,
// в зависимости от логического значения его выражения. Чтобы получить логическое значение
// которое определяет, какую строку отображает поле IF, поле IF проверит два числовых выражения на равенство.
// Мы предоставим два выражения в виде полей формулы, которые вложим внутрь поля IF.
auto leftExpression = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
leftExpression->AddArgument(2);
leftExpression->AddArgument(u"+");
leftExpression->AddArgument(3);

auto rightExpression = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
rightExpression->AddArgument(2.5);
rightExpression->AddArgument(u"*");
rightExpression->AddArgument(5.2);

// Затем мы создадим два аргумента поля, которые будут служить логическими (true/false) строками вывода для поля IF.
// Эти аргументы будут повторно использовать выходные значения наших числовых выражений.
auto trueOutput = System::MakeObject<Aspose::Words::Fields::FieldArgumentBuilder>();
trueOutput->AddText(u"True, both expressions amount to ");
trueOutput->AddField(leftExpression);

auto falseOutput = System::MakeObject<Aspose::Words::Fields::FieldArgumentBuilder>();
falseOutput->AddNode(System::MakeObject<Aspose::Words::Run>(doc, u"False, "));
falseOutput->AddField(leftExpression);
falseOutput->AddNode(System::MakeObject<Aspose::Words::Run>(doc, u" does not equal "));
falseOutput->AddField(rightExpression);

// Наконец, мы создадим еще один построитель полей для поля IF и объединим все выражения.
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

## См. также

* Class [FieldBuilder](../)
* Class [FieldBuilder](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
## FieldBuilder::AddArgument(const System::String\&) method


Добавляет аргумент поля.

```cpp
System::SharedPtr<Aspose::Words::Fields::FieldBuilder> Aspose::Words::Fields::FieldBuilder::AddArgument(const System::String &argument)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| argument | const System::String\& | Значение аргумента. |

## Примеры



Показывает, как создавать поля с помощью построителя полей, а затем вставлять их в документ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Ниже приведены три примера построения полей с использованием построителя полей.
// 1 -  Одинарное поле:
// Используйте построитель полей, чтобы добавить поле SYMBOL, которое отображает символ ƒ (флорин).
auto builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldSymbol);
builder->AddArgument(402);
builder->AddSwitch(u"\\f", u"Arial");
builder->AddSwitch(u"\\s", 25);
builder->AddSwitch(u"\\u");
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->get_FirstParagraph());

ASSERT_EQ(u" SYMBOL 402 \\f Arial \\s 25 \\u ", field->GetFieldCode());

// 2 -  Вложенное поле:
// Используйте построитель полей, чтобы создать поле формулы, используемое как внутреннее поле другим построителем полей.
auto innerFormulaBuilder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
innerFormulaBuilder->AddArgument(100);
innerFormulaBuilder->AddArgument(u"+");
innerFormulaBuilder->AddArgument(74);

// Создайте еще один построитель для другого поля SYMBOL и вставьте поле формулы
// которое мы создали выше, в поле SYMBOL в качестве его аргумента.
builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldSymbol);
builder->AddArgument(innerFormulaBuilder);
field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->AppendParagraph(System::String::Empty));

// Внешнее поле SYMBOL будет использовать результат поля формулы, 174, в качестве своего аргумента,
// что заставит поле отображать символ ® (знак регистрации), поскольку его номер символа — 174.
ASSERT_EQ(u" SYMBOL \u0013 = 100 + 74 \u0014\u0015 ", field->GetFieldCode());

// 3 -  Несколько вложенных полей и аргументов:
// Теперь мы используем построитель, чтобы создать поле IF, которое отображает одну из двух пользовательских строковых значений,
// в зависимости от логического значения его выражения. Чтобы получить логическое значение
// которое определяет, какую строку отображает поле IF, поле IF проверит два числовых выражения на равенство.
// Мы предоставим два выражения в виде полей формулы, которые вложим внутрь поля IF.
auto leftExpression = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
leftExpression->AddArgument(2);
leftExpression->AddArgument(u"+");
leftExpression->AddArgument(3);

auto rightExpression = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
rightExpression->AddArgument(2.5);
rightExpression->AddArgument(u"*");
rightExpression->AddArgument(5.2);

// Затем мы создадим два аргумента поля, которые будут служить логическими (true/false) строками вывода для поля IF.
// Эти аргументы будут повторно использовать выходные значения наших числовых выражений.
auto trueOutput = System::MakeObject<Aspose::Words::Fields::FieldArgumentBuilder>();
trueOutput->AddText(u"True, both expressions amount to ");
trueOutput->AddField(leftExpression);

auto falseOutput = System::MakeObject<Aspose::Words::Fields::FieldArgumentBuilder>();
falseOutput->AddNode(System::MakeObject<Aspose::Words::Run>(doc, u"False, "));
falseOutput->AddField(leftExpression);
falseOutput->AddNode(System::MakeObject<Aspose::Words::Run>(doc, u" does not equal "));
falseOutput->AddField(rightExpression);

// Наконец, мы создадим еще один построитель полей для поля IF и объединим все выражения.
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

## См. также

* Class [FieldBuilder](../)
* Class [FieldBuilder](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
## FieldBuilder::AddArgument(double) method


Добавляет аргумент поля.

```cpp
System::SharedPtr<Aspose::Words::Fields::FieldBuilder> Aspose::Words::Fields::FieldBuilder::AddArgument(double argument)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| argument | double | Значение аргумента. |

## Примеры



Показывает, как создавать поля с помощью построителя полей, а затем вставлять их в документ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Ниже приведены три примера построения полей с использованием построителя полей.
// 1 -  Одинарное поле:
// Используйте построитель полей, чтобы добавить поле SYMBOL, которое отображает символ ƒ (флорин).
auto builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldSymbol);
builder->AddArgument(402);
builder->AddSwitch(u"\\f", u"Arial");
builder->AddSwitch(u"\\s", 25);
builder->AddSwitch(u"\\u");
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->get_FirstParagraph());

ASSERT_EQ(u" SYMBOL 402 \\f Arial \\s 25 \\u ", field->GetFieldCode());

// 2 -  Вложенное поле:
// Используйте построитель полей, чтобы создать поле формулы, используемое как внутреннее поле другим построителем полей.
auto innerFormulaBuilder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
innerFormulaBuilder->AddArgument(100);
innerFormulaBuilder->AddArgument(u"+");
innerFormulaBuilder->AddArgument(74);

// Создайте еще один построитель для другого поля SYMBOL и вставьте поле формулы
// которое мы создали выше, в поле SYMBOL в качестве его аргумента.
builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldSymbol);
builder->AddArgument(innerFormulaBuilder);
field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->AppendParagraph(System::String::Empty));

// Внешнее поле SYMBOL будет использовать результат поля формулы, 174, в качестве своего аргумента,
// что заставит поле отображать символ ® (знак регистрации), поскольку его номер символа — 174.
ASSERT_EQ(u" SYMBOL \u0013 = 100 + 74 \u0014\u0015 ", field->GetFieldCode());

// 3 -  Несколько вложенных полей и аргументов:
// Теперь мы используем построитель, чтобы создать поле IF, которое отображает одну из двух пользовательских строковых значений,
// в зависимости от логического значения его выражения. Чтобы получить логическое значение
// которое определяет, какую строку отображает поле IF, поле IF проверит два числовых выражения на равенство.
// Мы предоставим два выражения в виде полей формулы, которые вложим внутрь поля IF.
auto leftExpression = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
leftExpression->AddArgument(2);
leftExpression->AddArgument(u"+");
leftExpression->AddArgument(3);

auto rightExpression = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
rightExpression->AddArgument(2.5);
rightExpression->AddArgument(u"*");
rightExpression->AddArgument(5.2);

// Затем мы создадим два аргумента поля, которые будут служить логическими (true/false) строками вывода для поля IF.
// Эти аргументы будут повторно использовать выходные значения наших числовых выражений.
auto trueOutput = System::MakeObject<Aspose::Words::Fields::FieldArgumentBuilder>();
trueOutput->AddText(u"True, both expressions amount to ");
trueOutput->AddField(leftExpression);

auto falseOutput = System::MakeObject<Aspose::Words::Fields::FieldArgumentBuilder>();
falseOutput->AddNode(System::MakeObject<Aspose::Words::Run>(doc, u"False, "));
falseOutput->AddField(leftExpression);
falseOutput->AddNode(System::MakeObject<Aspose::Words::Run>(doc, u" does not equal "));
falseOutput->AddField(rightExpression);

// Наконец, мы создадим еще один построитель полей для поля IF и объединим все выражения.
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

## См. также

* Class [FieldBuilder](../)
* Class [FieldBuilder](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
## FieldBuilder::AddArgument(int32_t) method


Добавляет аргумент поля.

```cpp
System::SharedPtr<Aspose::Words::Fields::FieldBuilder> Aspose::Words::Fields::FieldBuilder::AddArgument(int32_t argument)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| argument | int32_t | Значение аргумента. |

## Примеры



Показывает, как создавать поля с помощью построителя полей, а затем вставлять их в документ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Ниже приведены три примера построения полей с использованием построителя полей.
// 1 -  Одинарное поле:
// Используйте построитель полей, чтобы добавить поле SYMBOL, которое отображает символ ƒ (флорин).
auto builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldSymbol);
builder->AddArgument(402);
builder->AddSwitch(u"\\f", u"Arial");
builder->AddSwitch(u"\\s", 25);
builder->AddSwitch(u"\\u");
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->get_FirstParagraph());

ASSERT_EQ(u" SYMBOL 402 \\f Arial \\s 25 \\u ", field->GetFieldCode());

// 2 -  Вложенное поле:
// Используйте построитель полей, чтобы создать поле формулы, используемое как внутреннее поле другим построителем полей.
auto innerFormulaBuilder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
innerFormulaBuilder->AddArgument(100);
innerFormulaBuilder->AddArgument(u"+");
innerFormulaBuilder->AddArgument(74);

// Создайте еще один построитель для другого поля SYMBOL и вставьте поле формулы
// которое мы создали выше, в поле SYMBOL в качестве его аргумента.
builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldSymbol);
builder->AddArgument(innerFormulaBuilder);
field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->AppendParagraph(System::String::Empty));

// Внешнее поле SYMBOL будет использовать результат поля формулы, 174, в качестве своего аргумента,
// что заставит поле отображать символ ® (знак регистрации), поскольку его номер символа — 174.
ASSERT_EQ(u" SYMBOL \u0013 = 100 + 74 \u0014\u0015 ", field->GetFieldCode());

// 3 -  Несколько вложенных полей и аргументов:
// Теперь мы используем построитель, чтобы создать поле IF, которое отображает одну из двух пользовательских строковых значений,
// в зависимости от логического значения его выражения. Чтобы получить логическое значение
// которое определяет, какую строку отображает поле IF, поле IF проверит два числовых выражения на равенство.
// Мы предоставим два выражения в виде полей формулы, которые вложим внутрь поля IF.
auto leftExpression = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
leftExpression->AddArgument(2);
leftExpression->AddArgument(u"+");
leftExpression->AddArgument(3);

auto rightExpression = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
rightExpression->AddArgument(2.5);
rightExpression->AddArgument(u"*");
rightExpression->AddArgument(5.2);

// Затем мы создадим два аргумента поля, которые будут служить логическими (true/false) строками вывода для поля IF.
// Эти аргументы будут повторно использовать выходные значения наших числовых выражений.
auto trueOutput = System::MakeObject<Aspose::Words::Fields::FieldArgumentBuilder>();
trueOutput->AddText(u"True, both expressions amount to ");
trueOutput->AddField(leftExpression);

auto falseOutput = System::MakeObject<Aspose::Words::Fields::FieldArgumentBuilder>();
falseOutput->AddNode(System::MakeObject<Aspose::Words::Run>(doc, u"False, "));
falseOutput->AddField(leftExpression);
falseOutput->AddNode(System::MakeObject<Aspose::Words::Run>(doc, u" does not equal "));
falseOutput->AddField(rightExpression);

// Наконец, мы создадим еще один построитель полей для поля IF и объединим все выражения.
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

## См. также

* Class [FieldBuilder](../)
* Class [FieldBuilder](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
