---
title: "метод Aspose::Words::DocumentBuilder::InsertField"
linktitle: "InsertField"
second_title: "Справочник API Aspose.Words для C++"
description: "метод Aspose::Words::DocumentBuilder::InsertField. Вставляет поле Word в документ и при желании обновляет результат поля в C++."
type: docs
weight: 34000
url: /ru/cpp/aspose.words/documentbuilder/insertfield/
---
## DocumentBuilder::InsertField(Aspose::Words::Fields::FieldType, bool) method


Вставляет поле Word в документ и при необходимости обновляет результат поля.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::DocumentBuilder::InsertField(Aspose::Words::Fields::FieldType fieldType, bool updateField)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldType | Aspose::Words::Fields::FieldType | Тип поля для добавления. |
| updateField | bool | Указывает, следует ли обновлять поле немедленно. |

### ReturnValue

Объект [Field](../../../aspose.words.fields/field/), представляющий вставленное поле.
## Примечания


Этот метод вставляет поле в документ. Aspose.Words может обновлять поля большинства типов, но не все. Для получения более подробной информации см. перегрузку [InsertField()](../).

## Примеры



Показывает, как вставить поле в документ, используя FieldType.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте два поля, передавая флаг, определяющий, следует ли обновлять их при вставке builder'ом.
// В некоторых случаях обновление полей может быть вычислительно затратным, и может быть разумно отложить обновление.
doc->get_BuiltInDocumentProperties()->set_Author(u"John Doe");
builder->Write(u"This document was written by ");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, updateInsertedFieldsImmediately);

builder->InsertParagraph();
builder->Write(u"\nThis is page ");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldPage, updateInsertedFieldsImmediately);

ASSERT_EQ(u" AUTHOR ", doc->get_Range()->get_Fields()->idx_get(0)->GetFieldCode());
ASSERT_EQ(u" PAGE ", doc->get_Range()->get_Fields()->idx_get(1)->GetFieldCode());

if (updateInsertedFieldsImmediately)
{
    ASSERT_EQ(u"John Doe", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());
    ASSERT_EQ(u"1", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());
}
else
{
    ASSERT_EQ(System::String::Empty, doc->get_Range()->get_Fields()->idx_get(0)->get_Result());
    ASSERT_EQ(System::String::Empty, doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

    // Нам понадобится обновить эти поля вручную, используя методы обновления.
    doc->get_Range()->get_Fields()->idx_get(0)->Update();

    ASSERT_EQ(u"John Doe", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());

    doc->UpdateFields();

    ASSERT_EQ(u"1", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());
}
```

## См. также

* Class [Field](../../../aspose.words.fields/field/)
* Enum [FieldType](../../../aspose.words.fields/fieldtype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertField(const System::String\&) method


Вставляет поле Word в документ и обновляет результат поля.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::DocumentBuilder::InsertField(const System::String &fieldCode)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldCode | const System::String\& | Код поля для вставки (без фигурных скобок). |

### ReturnValue

Объект [Field](../../../aspose.words.fields/field/), представляющий вставленное поле.
## Примечания


Этот метод вставляет поле в документ и сразу обновляет результат поля. Aspose.Words может обновлять поля большинства типов, но не всех. Для получения более подробной информации см. перегрузку [InsertField()](../).

## Примеры



Показывает, как вставлять поля и перемещать курсор построителя документа к ним.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertField(u"MERGEFIELD MyMergeField1 \\* MERGEFORMAT");
builder->InsertField(u"MERGEFIELD MyMergeField2 \\* MERGEFORMAT");

// Переместите курсор к первому MERGEFIELD.
builder->MoveToMergeField(u"MyMergeField1", true, false);

// Обратите внимание, что курсор размещён сразу после первого MERGEFIELD и перед вторым.
ASPOSE_ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(1)->get_Start(), builder->get_CurrentNode());
ASPOSE_ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(0)->get_End(), builder->get_CurrentNode()->get_PreviousSibling());

// Если мы хотим отредактировать код поля или его содержимое с помощью построителя,
// его курсор должен находиться внутри поля.
// Чтобы разместить его внутри поля, нам нужно вызвать метод MoveTo построителя документа
// и передать в качестве аргумента начальный или разделительный узел поля.
builder->Write(u" Text between our merge fields. ");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.MergeFields.docx");
```


Показывает, как вставить поле в документ, используя код поля.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE \\@ \"dddd, MMMM dd, yyyy\"");

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());
ASSERT_EQ(u"DATE \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// Эта перегрузка метода InsertField автоматически обновляет вставленные поля.
ASSERT_TRUE((System::DateTime::get_Today() - System::DateTime::Parse(field->get_Result())).get_Days() <= 1);
```

## См. также

* Class [Field](../../../aspose.words.fields/field/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertField(const System::String\&, const System::String\&) method


Вставляет поле Word в документ без обновления результата поля.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::DocumentBuilder::InsertField(const System::String &fieldCode, const System::String &fieldValue)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldCode | const System::String\& | Код поля для вставки (без фигурных скобок). |
| fieldValue | const System::String\& | Значение поля для вставки. Передайте **null** для полей, у которых нет значения. |

### ReturnValue

Объект [Field](../../../aspose.words.fields/field/), представляющий вставленное поле.
## Примечания


[Fields](../../../aspose.words.fields/) in Microsoft Word documents consist of a field code and a field result. The field code is like a formula and the field result is like the value that the formula produces. The field code may also contain field switches that are like additional instructions to perform a specific action.

Вы можете переключаться между отображением кодов полей и их результатов в документе Microsoft Word, используя сочетание клавиш Alt+F9. Коды полей отображаются в фигурных скобках ( { } ).

Чтобы создать поле, необходимо указать тип поля, код поля и "заполнитель" значения поля. Если вы не уверены в синтаксисе конкретного кода поля, сначала создайте поле в Microsoft Word и переключитесь, чтобы увидеть его код.

Aspose.Words может вычислять результаты полей для большинства типов полей, но этот метод не обновляет результат поля автоматически. Поскольку результат поля не рассчитывается автоматически, от вас ожидается передать строковое значение (или даже пустую строку), которое будет вставлено в результат поля. Это значение останется в результате поля как заполнитель, пока поле не будет обновлено. Чтобы обновить результат поля, вы можете вызвать [Update](../../../aspose.words.fields/field/update/) у возвращённого объекта поля или [UpdateFields](../../document/updatefields/) для обновления полей во всём документе.

## Примеры



Показывает, как настроить нумерацию страниц в разделе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Section 1, page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 1, page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 1, page 3.");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Writeln(u"Section 2, page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 2, page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 2, page 3.");

// Переместите построитель документа в основной заголовок первого раздела,
// который будет отображаться на каждой странице этого раздела.
builder->MoveToSection(0);
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);

// Вставьте поле PAGE, которое будет отображать номер текущей страницы.
builder->Write(u"Page ");
builder->InsertField(u"PAGE", u"");

// Настройте раздел так, чтобы нумерация, отображаемая полями PAGE, начиналась с 5.
// Также настройте все поля PAGE так, чтобы они отображали номера страниц римскими цифрами верхнего регистра.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_RestartPageNumbering(true);
pageSetup->set_PageStartingNumber(5);
pageSetup->set_PageNumberStyle(Aspose::Words::NumberStyle::UppercaseRoman);

// Создайте еще один основной заголовок для второго раздела с другим полем PAGE.
builder->MoveToSection(1);
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
builder->Write(u" - ");
builder->InsertField(u"PAGE", u"");
builder->Write(u" - ");

// Настройте раздел так, чтобы нумерация, отображаемая полями PAGE, начиналась с 10.
// Также настройте все поля PAGE так, чтобы они отображали номера страниц арабскими цифрами.
pageSetup = doc->get_Sections()->idx_get(1)->get_PageSetup();
pageSetup->set_PageStartingNumber(10);
pageSetup->set_RestartPageNumbering(true);
pageSetup->set_PageNumberStyle(Aspose::Words::NumberStyle::Arabic);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageNumbering.docx");
```

## См. также

* Class [Field](../../../aspose.words.fields/field/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
