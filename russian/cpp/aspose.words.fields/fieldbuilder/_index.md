---
title: "класс Aspose::Words::Fields::FieldBuilder"
linktitle: "FieldBuilder"
second_title: "Справочник API Aspose.Words для C++"
description: "класс Aspose::Words::Fields::FieldBuilder. Создаёт поле из токенов кода поля (аргументы и переключатели). Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 20000
url: /ru/cpp/aspose.words.fields/fieldbuilder/
---
## FieldBuilder class


Создает поле из токенов кода поля (аргументы и переключатели). Чтобы узнать больше, посетите статью документации [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldBuilder : public Aspose::Words::Fields::IFieldBuildingBlock
```

## Методы

| Метод | Описание |
| --- | --- |
| [AddArgument](./addargument/)(const System::String\&) | Добавляет аргумент поля. |
| [AddArgument](./addargument/)(int32_t) | Добавляет аргумент поля. |
| [AddArgument](./addargument/)(double) | Добавляет аргумент поля. |
| [AddArgument](./addargument/)(const System::SharedPtr\<Aspose::Words::Fields::FieldBuilder\>\&) | Добавляет дочернее поле, представленное другим [FieldBuilder](./), в код поля. |
| [AddArgument](./addargument/)(const System::SharedPtr\<Aspose::Words::Fields::FieldArgumentBuilder\>\&) | Добавляет аргумент поля, представленный [FieldArgumentBuilder](../fieldargumentbuilder/), в код поля. |
| [AddSwitch](./addswitch/)(const System::String\&) | Добавляет переключатель поля. |
| [AddSwitch](./addswitch/)(const System::String\&, const System::String\&) | Добавляет переключатель поля. |
| [AddSwitch](./addswitch/)(const System::String\&, int32_t) | Добавляет переключатель поля. |
| [AddSwitch](./addswitch/)(const System::String\&, double) | Добавляет переключатель поля. |
| [BuildAndInsert](./buildandinsert/)(const System::SharedPtr\<Aspose::Words::Inline\>\&) | Создаёт и вставляет поле в документ перед указанным встроенным узлом. |
| [BuildAndInsert](./buildandinsert/)(const System::SharedPtr\<Aspose::Words::Paragraph\>\&) | Создаёт и вставляет поле в документ в конец указанного абзаца. |
| [FieldBuilder](./fieldbuilder/)(Aspose::Words::Fields::FieldType) | Инициализирует экземпляр класса [FieldBuilder](./). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
