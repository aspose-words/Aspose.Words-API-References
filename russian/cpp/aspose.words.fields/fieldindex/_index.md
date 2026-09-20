---
title: "Класс Aspose::Words::Fields::FieldIndex"
linktitle: "FieldIndex"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::Fields::FieldIndex. Реализует поле INDEX. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 59000
url: /ru/cpp/aspose.words.fields/fieldindex/
---
## FieldIndex class


Реализует поле INDEX. Чтобы узнать больше, посетите статью документации [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldIndex : public Aspose::Words::Fields::Field,
                   public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() | Получает или задает имя закладки, отмечающей часть документа, используемую для построения указателя. |
| [get_CrossReferenceSeparator](./get_crossreferenceseparator/)() | Получает или задает последовательность символов, используемую для разделения перекрёстных ссылок и других записей. |
| [get_DisplayResult](../field/get_displayresult/)() | Получает текст, представляющий отображаемый результат поля. |
| [get_End](../field/get_end/)() const | Получает узел, представляющий конец поля. |
| [get_EntryType](./get_entrytype/)() | Получает или задает тип записи указателя, используемый при построении указателя. |
| [get_FieldEnd](../field/get_fieldend/)() const | Получает узел, представляющий конец поля. |
| [get_FieldStart](../field/get_fieldstart/)() const | Получает узел, представляющий начало поля. |
| [get_Format](../field/get_format/)() | Получает объект [FieldFormat](../fieldformat/), который предоставляет типизированный доступ к форматированию поля. |
| [get_HasPageNumberSeparator](./get_haspagenumberseparator/)() | Возвращает значение, указывающее, переопределён ли разделитель номеров страниц в коде поля. |
| [get_HasSequenceName](./get_hassequencename/)() | Возвращает значение, указывающее, следует ли использовать последовательность при построении результата поля. |
| [get_Heading](./get_heading/)() | Получает или задает заголовок, который появляется в начале каждого набора записей для заданной буквы. |
| [get_IsDirty](../field/get_isdirty/)() | Получает или задает, является ли текущий результат поля более некорректным (устаревшим) из‑за других изменений, внесённых в документ. |
| [get_IsLocked](../field/get_islocked/)() | Получает или задает, заблокировано ли поле (не должно пересчитывать свой результат). |
| [get_LanguageId](./get_languageid/)() | Получает или задает идентификатор языка, используемый для создания указателя. |
| [get_LetterRange](./get_letterrange/)() | Получает или задает диапазон букв, ограничивающий указатель. |
| [get_LocaleId](../field/get_localeid/)() | Получает или задает LCID поля. |
| [get_NumberOfColumns](./get_numberofcolumns/)() | Получает или задает количество колонок на страницу, используемое при построении указателя. |
| [get_PageNumberListSeparator](./get_pagenumberlistseparator/)() | Получает или задает последовательность символов, используемую для разделения двух номеров страниц в списке номеров страниц. |
| [get_PageNumberSeparator](./get_pagenumberseparator/)() | Получает или задает последовательность символов, используемую для разделения записи указателя и её номера страницы. |
| [get_PageRangeSeparator](./get_pagerangeseparator/)() | Получает или задает последовательность символов, используемую для разделения начала и конца диапазона страниц. |
| [get_Result](../field/get_result/)() | Получает или задает текст, находящийся между разделителем поля и его концом. |
| [get_RunSubentriesOnSameLine](./get_runsubentriesonsameline/)() | Получает или задает, следует ли размещать подпункты в той же строке, что и основной пункт. |
| [get_Separator](../field/get_separator/)() | Получает узел, представляющий разделитель поля. Может быть **null**. |
| [get_SequenceName](./get_sequencename/)() | Получает или задает имя последовательности, номер которой включается в номер страницы. |
| [get_SequenceSeparator](./get_sequenceseparator/)() | Получает или задает последовательность символов, используемую для разделения номеров последовательностей и номеров страниц. |
| [get_Start](../field/get_start/)() const | Получает узел, представляющий начало поля. |
| virtual [get_Type](../field/get_type/)() const | Получает тип поля Microsoft Word. |
| [get_UseYomi](./get_useyomi/)() | Получает или задает, включить ли использование текста йоми для записей указателя. |
| [GetFieldCode](../field/getfieldcode/)() | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). Включены как код поля, так и результат дочерних полей. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля является последним дочерним элементом его родительского узла, возвращает родительский абзац. Если поле уже удалено, возвращает **null**. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FieldIndex::get_BookmarkName](./get_bookmarkname/). |
| [set_CrossReferenceSeparator](./set_crossreferenceseparator/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FieldIndex::get_CrossReferenceSeparator](./get_crossreferenceseparator/). |
| [set_EntryType](./set_entrytype/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FieldIndex::get_EntryType](./get_entrytype/). |
| [set_Heading](./set_heading/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FieldIndex::get_Heading](./get_heading/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Сеттер для [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Сеттер для [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LanguageId](./set_languageid/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FieldIndex::get_LanguageId](./get_languageid/). |
| [set_LetterRange](./set_letterrange/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FieldIndex::get_LetterRange](./get_letterrange/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Сеттер для [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_NumberOfColumns](./set_numberofcolumns/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FieldIndex::get_NumberOfColumns](./get_numberofcolumns/). |
| [set_PageNumberListSeparator](./set_pagenumberlistseparator/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FieldIndex::get_PageNumberListSeparator](./get_pagenumberlistseparator/). |
| [set_PageNumberSeparator](./set_pagenumberseparator/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FieldIndex::get_PageNumberSeparator](./get_pagenumberseparator/). |
| [set_PageRangeSeparator](./set_pagerangeseparator/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FieldIndex::get_PageRangeSeparator](./get_pagerangeseparator/). |
| [set_Result](../field/set_result/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_RunSubentriesOnSameLine](./set_runsubentriesonsameline/)(bool) | Сеттер для [Aspose::Words::Fields::FieldIndex::get_RunSubentriesOnSameLine](./get_runsubentriesonsameline/). |
| [set_SequenceName](./set_sequencename/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FieldIndex::get_SequenceName](./get_sequencename/). |
| [set_SequenceSeparator](./set_sequenceseparator/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FieldIndex::get_SequenceSeparator](./get_sequenceseparator/). |
| [set_UseYomi](./set_useyomi/)(bool) | Сеттер для [Aspose::Words::Fields::FieldIndex::get_UseYomi](./get_useyomi/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Выполняет отсоединение поля. |
| [Update](../field/update/)() | Выполняет обновление поля. Вызывает исключение, если поле уже обновляется. |
| [Update](../field/update/)(bool) | Выполняет обновление поля. Выбрасывает исключение, если поле уже обновляется. |

## Примеры



Показывает, как создать поле INDEX и затем использовать поля XE для заполнения его записями.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Создайте поле INDEX, которое будет отображать запись для каждого найденного в документе поля XE.
// Каждая запись будет отображать значение свойства Text поля XE слева
// и страницу, содержащую поле XE, справа.
// Если у полей XE одинаковое значение в их свойстве "Text",
// поле INDEX сгруппирует их в одну запись.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// Настройте поле INDEX так, чтобы оно отображало только поля XE, находящиеся в пределах
// закладки с именем "MainBookmark" и у которых свойство "EntryType" имеет значение "A".
// Для полей INDEX и XE свойство "EntryType" использует только первый символ строкового значения.
index->set_BookmarkName(u"MainBookmark");
index->set_EntryType(u"A");

ASSERT_EQ(u" INDEX  \\b MainBookmark \\f A", index->GetFieldCode());

// На новой странице начните закладку с именем, соответствующим значению
// свойства "BookmarkName" поля INDEX.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(u"MainBookmark");

// Поле INDEX подхватит эту запись, потому что она находится внутри закладки,
// и её тип записи также соответствует типу записи поля INDEX.
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Index entry 1");
indexEntry->set_EntryType(u"A");

ASSERT_EQ(u" XE  \"Index entry 1\" \\f A", indexEntry->GetFieldCode());

// Вставьте поле XE, которое не появится в INDEX, потому что типы записей не совпадают.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Index entry 2");
indexEntry->set_EntryType(u"B");

// Закончите закладку и вставьте поле XE после неё.
// Оно того же типа, что и поле INDEX, но не появится
// поскольку находится за пределами границ закладки.
builder->EndBookmark(u"MainBookmark");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Index entry 3");
indexEntry->set_EntryType(u"A");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.Filtering.docx");
```


Показывает, как заполнить поле INDEX записями с помощью полей XE и также изменить его внешний вид.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Создайте поле INDEX, которое будет отображать запись для каждого найденного в документе поля XE.
// Каждая запись будет отображать значение свойства Text поля XE слева,
// а номер страницы, содержащей поле XE, — справа.
// Если у полей XE одинаковое значение в их свойстве "Text",
// поле INDEX сгруппирует их в одну запись.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));
index->set_LanguageId(u"1033");

// Установка значения этого свойства в "A" сгруппирует все записи по первой букве,
// и разместит эту букву в верхнем регистре над каждой группой.
index->set_Heading(u"A");

// Установите, чтобы таблица, созданная полем INDEX, охватывала 2 столбца.
index->set_NumberOfColumns(u"2");

// Установите, чтобы любые записи, начинающиеся с букв вне диапазона "a-c", были опущены.
index->set_LetterRange(u"a-c");

ASSERT_EQ(u" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index->GetFieldCode());

// Следующие два поля XE появятся под заголовком "A",
// при этом их соответствующее форматирование текста также будет применено к номерам страниц.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Apple");
indexEntry->set_IsItalic(true);

ASSERT_EQ(u" XE  Apple \\i", indexEntry->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Apricot");
indexEntry->set_IsBold(true);

ASSERT_EQ(u" XE  Apricot \\b", indexEntry->GetFieldCode());

// Оба следующих поля XE будут под заголовками "B" и "C" в содержании таблицы полей INDEX.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Banana");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Cherry");

// Поля INDEX сортируют все записи в алфавитном порядке, поэтому эта запись появится под "A" вместе с другими двумя.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Avocado");

// Эта запись не появится, потому что она начинается с буквы "D",
// что находится вне диапазона символов "a-c", определяемого свойством LetterRange поля INDEX.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Durian");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.Formatting.docx");
```

## См. также

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
