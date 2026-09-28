---
title: "Метод Aspose::Words::Paragraph::JoinRunsWithSameFormatting"
linktitle: "JoinRunsWithSameFormatting"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Paragraph::JoinRunsWithSameFormatting. Объединяет фрагменты текста с одинаковым форматированием в абзаце в C++."
type: docs
weight: 31000
url: /ru/cpp/aspose.words/paragraph/joinrunswithsameformatting/
---
## Paragraph::JoinRunsWithSameFormatting() method


Объединяет участки текста с одинаковым форматированием в абзаце.

```cpp
int32_t Aspose::Words::Paragraph::JoinRunsWithSameFormatting()
```


### ReturnValue

Количество выполненных объединений. Когда объединяются **N** соседних участков, они считаются как **N - 1** объединений.

## Примеры



Показывает, как упростить абзацы, объединяя избыточные фрагменты.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте четыре фрагмента текста в абзац.
builder->Write(u"Run 1. ");
builder->Write(u"Run 2. ");
builder->Write(u"Run 3. ");
builder->Write(u"Run 4. ");

// Если открыть этот документ в Microsoft Word, абзац будет выглядеть как единое непрерывное тело текста.
// Однако он будет состоять из четырёх отдельных фрагментов с одинаковым форматированием. Фрагментированные абзацы такого типа
// могут возникать, когда мы вручную редактируем части одного абзаца многократно в Microsoft Word.
System::SharedPtr<Aspose::Words::Paragraph> para = builder->get_CurrentParagraph();

ASSERT_EQ(4, para->get_Runs()->get_Count());

// Измените стиль последнего фрагмента, чтобы отличить его от первых трёх.
para->get_Runs()->idx_get(3)->get_Font()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Emphasis);

// Мы можем вызвать метод "JoinRunsWithSameFormatting", чтобы оптимизировать содержимое документа
// объединяя похожие фрагменты в один, уменьшая их общее количество.
// Этот метод также возвращает количество фрагментов, объединённых этим методом.
// Эти два объединения произошли для комбинирования фрагментов #1, #2 и #3,
// пропуская Run #4, потому что у него несовместимый стиль.
ASSERT_EQ(2, para->JoinRunsWithSameFormatting());

// Количество оставшихся запусков будет равно исходному количеству
// минус количество объединений запусков, выполненных методом "JoinRunsWithSameFormatting".
ASSERT_EQ(2, para->get_Runs()->get_Count());
ASSERT_EQ(u"Run 1. Run 2. Run 3. ", para->get_Runs()->idx_get(0)->get_Text());
ASSERT_EQ(u"Run 4. ", para->get_Runs()->idx_get(1)->get_Text());
```

## См. также

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Paragraph::JoinRunsWithSameFormatting(const System::SharedPtr\<Aspose::Words::JoinRunsOptions\>\&) method


Объединяет участки текста с одинаковым форматированием в абзаце.

```cpp
int32_t Aspose::Words::Paragraph::JoinRunsWithSameFormatting(const System::SharedPtr<Aspose::Words::JoinRunsOptions> &options)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| параметры | const System::SharedPtr\<Aspose::Words::JoinRunsOptions\>\& | Дополнительные параметры |

### ReturnValue

Количество выполненных объединений. Когда объединяются **N** соседних участков, они считаются как **N - 1** объединений.

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

* Class [JoinRunsOptions](../../joinrunsoptions/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
