---
title: "Класс Aspose::Words::JoinRunsOptions"
linktitle: "JoinRunsOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::JoinRunsOptions. Предоставляет флаги конфигурации для операции объединения пробегов в C++."
type: docs
weight: 38500
url: /ru/cpp/aspose.words/joinrunsoptions/
---
## JoinRunsOptions class


Предоставляет флаги конфигурации для операции объединения пробегов.

```cpp
class JoinRunsOptions : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_IgnoreInsignificant](./get_ignoreinsignificant/)() const | Истина указывает, что незначительные атрибуты всех пробегов будут игнорироваться при объединении пробегов с одинаковым форматированием. |
| [get_IgnoreRedundant](./get_ignoreredundant/)() const | Истина указывает, что избыточные атрибуты всех пробегов будут игнорироваться при объединении пробегов с одинаковым форматированием. |
| [get_IgnoreSpacing](./get_ignorespacing/)() const | Истина указывает, что атрибуты интервалов всех пробегов будут игнорироваться при объединении пробегов с одинаковым форматированием. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [JoinRunsOptions](./joinrunsoptions/)() |  |
| [set_IgnoreInsignificant](./set_ignoreinsignificant/)(bool) | Истина указывает, что незначительные атрибуты всех пробегов будут игнорироваться при объединении пробегов с одинаковым форматированием. |
| [set_IgnoreRedundant](./set_ignoreredundant/)(bool) | Истина указывает, что избыточные атрибуты всех пробегов будут игнорироваться при объединении пробегов с одинаковым форматированием. |
| [set_IgnoreSpacing](./set_ignorespacing/)(bool) | Истина указывает, что атрибуты интервалов всех пробегов будут игнорироваться при объединении пробегов с одинаковым форматированием. |
| static [Type](./type/)() |  |

## Примеры



Показывает, как объединять пробеги с одинаковым форматированием, игнорируя избыточные и незначительные атрибуты.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Создайте пробеги с одинаковым видимым форматированием, но с некоторыми внутренними различиями.
builder->get_Font()->set_Name(u"Arial");
builder->get_Font()->set_Size(12);
builder->Write(u"Hello ");
builder->Write(u"world");

// Проверьте пробеги перед объединением.
ASSERT_EQ(2, doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->get_Count());
ASSERT_EQ(u"Hello ", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Text());
ASSERT_EQ(u"world", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(1)->get_Text());

// Настройте параметры для игнорирования избыточных и незначительных атрибутов во время объединения.
auto options = System::MakeObject<Aspose::Words::JoinRunsOptions>();
options->set_IgnoreRedundant(true);
// Игнорировать избыточные свойства пробегов, которые не влияют на внешний вид.
options->set_IgnoreInsignificant(true);
// Игнорировать незначительные различия, такие как пробеги, содержащие только пробелы.

// Объедините участки, имеющие одинаковое видимое форматирование, используя расширенные параметры.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->JoinRunsWithSameFormatting(options);

// Проверьте, что участки были успешно объединены.
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->get_Count());
ASSERT_EQ(u"Hello world", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Text());

doc->Save(get_ArtifactsDir() + u"Paragraph.JoinRunsWithSameFormattingWithOptions.docx");
```

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
