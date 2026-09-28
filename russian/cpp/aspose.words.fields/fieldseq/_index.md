---
title: "Aspose::Words::Fields::FieldSeq class"
linktitle: "FieldSeq"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldSeq class. Реализует поле SEQ. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 91000
url: /ru/cpp/aspose.words.fields/fieldseq/
---
## FieldSeq class


Реализует поле SEQ. Чтобы узнать больше, посетите статью документации [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldSeq : public Aspose::Words::Fields::Field,
                 public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() | Получает или задаёт имя закладки, которое ссылается на элемент в другом месте документа, а не в текущем расположении. |
| [get_DisplayResult](../field/get_displayresult/)() | Получает текст, представляющий отображаемый результат поля. |
| [get_End](../field/get_end/)() const | Получает узел, представляющий конец поля. |
| [get_FieldEnd](../field/get_fieldend/)() const | Получает узел, представляющий конец поля. |
| [get_FieldStart](../field/get_fieldstart/)() const | Получает узел, представляющий начало поля. |
| [get_Format](../field/get_format/)() | Получает объект [FieldFormat](../fieldformat/), который предоставляет типизированный доступ к форматированию поля. |
| [get_InsertNextNumber](./get_insertnextnumber/)() | Получает или задаёт, следует ли вставлять следующий номер последовательности для указанного элемента. |
| [get_IsDirty](../field/get_isdirty/)() | Получает или задает, является ли текущий результат поля более некорректным (устаревшим) из‑за других изменений, внесённых в документ. |
| [get_IsLocked](../field/get_islocked/)() | Получает или задает, заблокировано ли поле (не должно пересчитывать свой результат). |
| [get_LocaleId](../field/get_localeid/)() | Получает или задает LCID поля. |
| [get_ResetHeadingLevel](./get_resetheadinglevel/)() | Получает или задаёт целое число, представляющее уровень заголовка, к которому следует сбросить номер последовательности. Возвращает -1, если число отсутствует. |
| [get_ResetNumber](./get_resetnumber/)() | Получает или задаёт целое число, к которому следует сбросить номер последовательности. Возвращает -1, если число отсутствует. |
| [get_Result](../field/get_result/)() | Получает или задает текст, находящийся между разделителем поля и его концом. |
| [get_Separator](../field/get_separator/)() | Получает узел, представляющий разделитель поля. Может быть **null**. |
| [get_SequenceIdentifier](./get_sequenceidentifier/)() | Получает или задаёт имя, присвоенное серии элементов, которые должны быть пронумерованы. |
| [get_Start](../field/get_start/)() const | Получает узел, представляющий начало поля. |
| virtual [get_Type](../field/get_type/)() const | Получает тип поля Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). Включены как код поля, так и результат дочерних полей. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля является последним дочерним элементом его родительского узла, возвращает родительский абзац. Если поле уже удалено, возвращает **null**. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FieldSeq::get_BookmarkName](./get_bookmarkname/). |
| [set_InsertNextNumber](./set_insertnextnumber/)(bool) | Сеттер для [Aspose::Words::Fields::FieldSeq::get_InsertNextNumber](./get_insertnextnumber/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Сеттер для [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Сеттер для [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Сеттер для [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_ResetHeadingLevel](./set_resetheadinglevel/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FieldSeq::get_ResetHeadingLevel](./get_resetheadinglevel/). |
| [set_ResetNumber](./set_resetnumber/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FieldSeq::get_ResetNumber](./get_resetnumber/). |
| [set_Result](../field/set_result/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SequenceIdentifier](./set_sequenceidentifier/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FieldSeq::get_SequenceIdentifier](./get_sequenceidentifier/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Выполняет отсоединение поля. |
| [Update](../field/update/)() | Выполняет обновление поля. Вызывает исключение, если поле уже обновляется. |
| [Update](../field/update/)(bool) | Выполняет обновление поля. Выбрасывает исключение, если поле уже обновляется. |

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


Показывает создание нумерации с использованием полей SEQ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Поля SEQ отображают счётчик, который увеличивается на каждом поле SEQ.
// Эти поля также поддерживают отдельные счётчики для каждой уникальной именованной последовательности.
// идентифицировано свойством "SequenceIdentifier" поля SEQ.
// Вставьте поле SEQ, которое будет отображать текущее значение счётчика "MySequence",
// после использования свойства "ResetNumber" для установки его в 100.
builder->Write(u"#");
auto fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_ResetNumber(u"100");
fieldSeq->Update();

ASSERT_EQ(u" SEQ  MySequence \\r 100", fieldSeq->GetFieldCode());
ASSERT_EQ(u"100", fieldSeq->get_Result());

// Отобразите следующее число в этой последовательности с помощью другого поля SEQ.
builder->Write(u", #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->Update();

ASSERT_EQ(u"101", fieldSeq->get_Result());

// Вставьте заголовок уровня 1.
builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"This level 1 heading will reset MySequence to 1");
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));

// Вставьте ещё одно поле SEQ из той же последовательности и настройте его сбрасывать счётчик до 1 при каждом заголовке.
builder->Write(u"\n#");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_ResetHeadingLevel(u"1");
fieldSeq->Update();

// Указанный выше заголовок — заголовок уровня 1, поэтому счётчик для этой последовательности сбрасывается до 1.
ASSERT_EQ(u" SEQ  MySequence \\s 1", fieldSeq->GetFieldCode());
ASSERT_EQ(u"1", fieldSeq->get_Result());

// Перейдите к следующему числу этой последовательности.
builder->Write(u", #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_InsertNextNumber(true);
fieldSeq->Update();

ASSERT_EQ(u" SEQ  MySequence \\n", fieldSeq->GetFieldCode());
ASSERT_EQ(u"2", fieldSeq->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SEQ.ResetNumbering.docx");
```


Показывает, как комбинировать оглавление и поля последовательности.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Поле TOC может создавать запись в своей таблице содержимого для каждого найденного в документе поля SEQ.
// Каждая запись содержит абзац, в котором находится поле SEQ,
// и номер страницы, на которой появляется поле.
auto fieldToc = System::ExplicitCast<Aspose::Words::Fields::FieldToc>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true));

// Настройте это поле TOC так, чтобы у него было свойство SequenceIdentifier со значением "MySequence".
fieldToc->set_TableOfFiguresLabel(u"MySequence");

// Настройте это поле TOC так, чтобы оно выбирало только поля SEQ, находящиеся в пределах закладки
// с именем "TOCBookmark".
fieldToc->set_BookmarkName(u"TOCBookmark");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

ASSERT_EQ(u" TOC  \\c MySequence \\b TOCBookmark", fieldToc->GetFieldCode());

// Поля SEQ отображают счётчик, который увеличивается на каждом поле SEQ.
// Эти поля также поддерживают отдельные счётчики для каждой уникальной именованной последовательности.
// идентифицировано свойством "SequenceIdentifier" поля SEQ.
// Вставьте поле SEQ, у которого идентификатор последовательности совпадает с
// свойством TableOfFiguresLabel у TOC. Это поле не создаст запись в оглавлении, поскольку оно находится за пределами
// границ закладки, обозначенных "BookmarkName".
builder->Write(u"MySequence #");
auto fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
builder->Writeln(u", will not show up in the TOC because it is outside of the bookmark.");

builder->StartBookmark(u"TOCBookmark");

// Последовательность этого поля SEQ совпадает со свойством "TableOfFiguresLabel" у TOC и находится в пределах границ закладки.
// Абзац, содержащий это поле, появится в оглавлении как запись.
builder->Write(u"MySequence #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
builder->Writeln(u", will show up in the TOC next to the entry for the above caption.");

// Последовательность этого поля SEQ не совпадает со свойством "TableOfFiguresLabel" у TOC,
// но находится в пределах границ закладки. Его абзац не появится в оглавлении как запись.
builder->Write(u"MySequence #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"OtherSequence");
builder->Writeln(u", will not show up in the TOC because it's from a different sequence identifier.");

// Последовательность этого поля SEQ совпадает со свойством "TableOfFiguresLabel" у TOC и находится в пределах границ закладки.
// Это поле также ссылается на другую закладку. Содержимое этой закладки появится в записи оглавления для этого поля SEQ.
// Само поле SEQ не будет отображать содержимое этой закладки.
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_BookmarkName(u"SEQBookmark");
ASSERT_EQ(u" SEQ  MySequence SEQBookmark", fieldSeq->GetFieldCode());

// Создайте закладку с содержимым, которое появится в записи оглавления из-за того, что вышеуказанное поле SEQ ссылается на неё.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(u"SEQBookmark");
builder->Write(u"MySequence #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
builder->Writeln(u", text from inside SEQBookmark.");
builder->EndBookmark(u"SEQBookmark");

builder->EndBookmark(u"TOCBookmark");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SEQ.Bookmark.docx");
```

## См. также

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
