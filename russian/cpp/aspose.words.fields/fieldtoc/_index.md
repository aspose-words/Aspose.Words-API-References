---
title: "Aspose::Words::Fields::FieldToc класс"
linktitle: "FieldToc"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldToc класс. Реализует поле TOC. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 105000
url: /ru/cpp/aspose.words.fields/fieldtoc/
---
## FieldToc class


Реализует поле TOC. Чтобы узнать больше, посетите статью документации [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldToc : public Aspose::Words::Fields::Field,
                 public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Методы

| Метод | Описание |
| --- | --- |
| [FieldToc](./fieldtoc/)() |  |
| [get_BookmarkName](./get_bookmarkname/)() | Получает имя закладки, которое отмечает часть документа, используемую для построения таблицы. |
| [get_CaptionlessTableOfFiguresLabel](./get_captionlesstableoffigureslabel/)() | Получает или задает имя идентификатора последовательности, используемого при построении списка иллюстраций, который не включает метку и номер подписи. |
| [get_CustomStyles](./get_customstyles/)() | Получает список стилей, отличных от встроенных стилей заголовков, которые включаются в оглавление. |
| [get_DisplayResult](../field/get_displayresult/)() | Получает текст, представляющий отображаемый результат поля. |
| [get_End](../field/get_end/)() const | Получает узел, представляющий конец поля. |
| [get_EntryIdentifier](./get_entryidentifier/)() | Получает строку, которая должна соответствовать типовым идентификаторам включаемых полей TC. |
| [get_EntryLevelRange](./get_entrylevelrange/)() | Получает диапазон уровней записей оглавления, которые будут включены. |
| [get_EntrySeparator](./get_entryseparator/)() | Получает последовательность символов, разделяющих запись и её номер страницы. |
| [get_FieldEnd](../field/get_fieldend/)() const | Получает узел, представляющий конец поля. |
| [get_FieldStart](../field/get_fieldstart/)() const | Получает узел, представляющий начало поля. |
| [get_Format](../field/get_format/)() | Получает объект [FieldFormat](../fieldformat/), который предоставляет типизированный доступ к форматированию поля. |
| [get_HeadingLevelRange](./get_headinglevelrange/)() | Получает диапазон уровней заголовков для включения. |
| [get_HideInWebLayout](./get_hideinweblayout/)() | Получает, следует ли скрывать табуляцию и номера страниц в режиме веб‑разметки. |
| [get_InsertHyperlinks](./get_inserthyperlinks/)() | Получает, следует ли делать записи оглавления гиперссылками. |
| [get_IsDirty](../field/get_isdirty/)() | Получает или задает, является ли текущий результат поля более некорректным (устаревшим) из‑за других изменений, внесённых в документ. |
| [get_IsLocked](../field/get_islocked/)() | Получает или задает, заблокировано ли поле (не должно пересчитывать свой результат). |
| [get_LocaleId](../field/get_localeid/)() | Получает или задает LCID поля. |
| [get_PageNumberOmittingLevelRange](./get_pagenumberomittinglevelrange/)() | Получает диапазон уровней записей оглавления, из которых следует опустить номера страниц. |
| [get_PrefixedSequenceIdentifier](./get_prefixedsequenceidentifier/)() | Получает или задает идентификатор последовательности, к номеру страницы записи которой следует добавить префикс. |
| [get_PreserveLineBreaks](./get_preservelinebreaks/)() | Получает, следует ли сохранять символы новой строки внутри записей таблицы. |
| [get_PreserveTabs](./get_preservetabs/)() | Получает, следует ли сохранять табуляцию внутри записей таблицы. |
| [get_Result](../field/get_result/)() | Получает или задает текст, находящийся между разделителем поля и его концом. |
| [get_Separator](../field/get_separator/)() | Получает узел, представляющий разделитель поля. Может быть **null**. |
| [get_SequenceSeparator](./get_sequenceseparator/)() | Получает или задает последовательность символов, используемую для разделения номеров последовательностей и номеров страниц. |
| [get_Start](../field/get_start/)() const | Получает узел, представляющий начало поля. |
| [get_TableOfFiguresLabel](./get_tableoffigureslabel/)() | Получает или задает имя идентификатора последовательности, используемого при построении списка иллюстраций. |
| virtual [get_Type](../field/get_type/)() const | Получает тип поля Microsoft Word. |
| [get_UseParagraphOutlineLevel](./get_useparagraphoutlinelevel/)() | Получает, следует ли использовать примененный уровень структуры абзаца. |
| [GetFieldCode](../field/getfieldcode/)() | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). Включены как код поля, так и результат дочерних полей. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля является последним дочерним элементом его родительского узла, возвращает родительский абзац. Если поле уже удалено, возвращает **null**. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Устанавливает имя закладки, которое отмечает часть документа, используемую для построения таблицы. |
| [set_CaptionlessTableOfFiguresLabel](./set_captionlesstableoffigureslabel/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FieldToc::get_CaptionlessTableOfFiguresLabel](./get_captionlesstableoffigureslabel/). |
| [set_CustomStyles](./set_customstyles/)(const System::String\&) | Устанавливает список стилей, отличных от встроенных стилей заголовков, которые включаются в оглавление. |
| [set_EntryIdentifier](./set_entryidentifier/)(const System::String\&) | Устанавливает строку, которая должна соответствовать типовым идентификаторам включаемых полей TC. |
| [set_EntryLevelRange](./set_entrylevelrange/)(const System::String\&) | Устанавливает диапазон уровней записей оглавления, которые будут включены. |
| [set_EntrySeparator](./set_entryseparator/)(const System::String\&) | Устанавливает последовательность символов, разделяющих запись и её номер страницы. |
| [set_HeadingLevelRange](./set_headinglevelrange/)(const System::String\&) | Устанавливает диапазон уровней заголовков для включения. |
| [set_HideInWebLayout](./set_hideinweblayout/)(bool) | Устанавливает, следует ли скрывать табуляцию и номера страниц в режиме веб‑разметки. |
| [set_InsertHyperlinks](./set_inserthyperlinks/)(bool) | Устанавливает, следует ли делать записи оглавления гиперссылками. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Сеттер для [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Сеттер для [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Сеттер для [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_PageNumberOmittingLevelRange](./set_pagenumberomittinglevelrange/)(const System::String\&) | Устанавливает диапазон уровней записей оглавления, из которых опускаются номера страниц. |
| [set_PrefixedSequenceIdentifier](./set_prefixedsequenceidentifier/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FieldToc::get_PrefixedSequenceIdentifier](./get_prefixedsequenceidentifier/). |
| [set_PreserveLineBreaks](./set_preservelinebreaks/)(bool) | Устанавливает, сохранять ли символы новой строки внутри записей таблицы. |
| [set_PreserveTabs](./set_preservetabs/)(bool) | Устанавливает, сохранять ли табуляцию внутри записей таблицы. |
| [set_Result](../field/set_result/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SequenceSeparator](./set_sequenceseparator/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FieldToc::get_SequenceSeparator](./get_sequenceseparator/). |
| [set_TableOfFiguresLabel](./set_tableoffigureslabel/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FieldToc::get_TableOfFiguresLabel](./get_tableoffigureslabel/). |
| [set_UseParagraphOutlineLevel](./set_useparagraphoutlinelevel/)(bool) | Устанавливает, использовать ли применённый уровень структуры абзаца. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Выполняет отсоединение поля. |
| [Update](../field/update/)() | Выполняет обновление поля. Вызывает исключение, если поле уже обновляется. |
| [Update](../field/update/)(bool) | Выполняет обновление поля. Выбрасывает исключение, если поле уже обновляется. |
| [UpdatePageNumbers](./updatepagenumbers/)() | Обновляет номера страниц для элементов в этом оглавлении. |

## Примеры



Показывает, как заполнить поле TOC записями, используя поля SEQ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Поле TOC может создавать запись в своей таблице содержимого для каждого найденного в документе поля SEQ.
// Каждая запись содержит абзац, включающий поле SEQ, и номер страницы, на которой появляется поле.
auto fieldToc = System::ExplicitCast<Aspose::Words::Fields::FieldToc>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true));

// Поля SEQ отображают счётчик, который увеличивается на каждом поле SEQ.
// Эти поля также поддерживают отдельные счётчики для каждой уникальной именованной последовательности.
// идентифицировано свойством "SequenceIdentifier" поля SEQ.
// Используйте свойство "TableOfFiguresLabel", чтобы задать основную последовательность для оглавления.
// Теперь это оглавление будет создавать записи только из полей SEQ, у которых свойство "SequenceIdentifier" установлено в "MySequence".
fieldToc->set_TableOfFiguresLabel(u"MySequence");

// Мы можем задать другую последовательность полей SEQ в свойстве "PrefixedSequenceIdentifier".
// Поля SEQ из этой префиксной последовательности не будут создавать записи в оглавлении.
// Каждая запись оглавления, созданная из поля SEQ основной последовательности, теперь также будет отображать счётчик, который
// префиксная последовательность находится на текущем значении в основном поле SEQ, которое создало запись.
fieldToc->set_PrefixedSequenceIdentifier(u"PrefixSequence");

// Каждая запись оглавления будет отображать счётчик префиксной последовательности сразу слева
// от номера страницы, на которой находится поле SEQ основной последовательности.
// Мы можем указать пользовательский разделитель, который будет отображаться между этими двумя числами.
fieldToc->set_SequenceSeparator(u">");

ASSERT_EQ(u" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// Существует два способа использования полей SEQ для заполнения этого оглавления.
// 1 - Вставка поля SEQ, принадлежащего префиксной последовательности оглавления:
// Это поле увеличит счётчик последовательности SEQ для "PrefixSequence" на 1.
// Поскольку это поле не принадлежит основной последовательности, идентифицированной
// свойством "TableOfFiguresLabel" оглавления, оно не будет отображаться как запись.
auto fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"PrefixSequence");
builder->InsertParagraph();

ASSERT_EQ(u" SEQ  PrefixSequence", fieldSeq->GetFieldCode());

// 2 - Вставка поля SEQ, принадлежащего основной последовательности оглавления:
// Это поле SEQ создаст запись в оглавлении.
// Запись оглавления будет содержать абзац, в котором находится поле SEQ, и номер страницы, на которой оно расположено.
// Эта запись также будет отображать счётчик, на котором сейчас находится префиксная последовательность,
// отделённый от номера страницы значением свойства SeqenceSeparator оглавления.
// Счётчик "PrefixSequence" равен 1, это поле SEQ основной последовательности находится на странице 2,
// а разделитель — ">", поэтому запись будет отображать "1>2".
builder->Write(u"First TOC entry, MySequence #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");

ASSERT_EQ(u" SEQ  MySequence", fieldSeq->GetFieldCode());

// Вставьте страницу, увеличьте префиксную последовательность на 2 и затем вставьте поле SEQ, чтобы создать запись в оглавлении.
// Префиксная последовательность теперь равна 2, а поле SEQ основной последовательности находится на странице 3,
// поэтому запись оглавления будет отображать "2>3" в своём номере страницы.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"PrefixSequence");
builder->InsertParagraph();
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
builder->Write(u"Second TOC entry, MySequence #");
fieldSeq->set_SequenceIdentifier(u"MySequence");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.TOC.SEQ.docx");
```

## См. также

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
