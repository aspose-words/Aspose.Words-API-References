---
title: "Aspose::Words::Document::UpdateFields метод"
linktitle: "UpdateFields"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Document::UpdateFields метод. Обновляет значения полей во всём документе в C++."
type: docs
weight: 96000
url: /ru/cpp/aspose.words/document/updatefields/
---
## Document::UpdateFields method


Обновляет значения полей во всём документе.

```cpp
void Aspose::Words::Document::UpdateFields()
```

## Примечания


Когда вы открываете, изменяете и затем сохраняете документ, Aspose.Words не обновляет поля автоматически, а оставляет их неизменными. Поэтому обычно следует вызвать этот метод перед сохранением, если вы программно изменили документ и хотите убедиться, что правильные (вычисленные) значения полей отображаются в сохранённом документе.

Нет необходимости обновлять поля после выполнения слияния почты, поскольку слияние почты является видом обновления полей и автоматически обновляет все поля в документе.

Этот метод не обновляет все типы полей. Для подробного списка поддерживаемых типов полей см. Руководство программиста.

Этот метод не обновляет поля, связанные с алгоритмами разметки страниц (например, PAGE, PAGES, PAGEREF). Поля, связанные с разметкой страниц, обновляются при рендеринге документа или вызове [UpdatePageLayout](../updatepagelayout/).

Используйте метод [NormalizeFieldTypes](../normalizefieldtypes/) перед обновлением полей, если в документе произошли изменения, повлиявшие на типы полей.

Чтобы обновить поля в определённой части документа, используйте [UpdateFields](../../range/updatefields/).

## Примеры



Показывает, как вставить оглавление (TOC) в документ, используя стили заголовков в качестве записей.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте оглавление для первой страницы документа.
// Настройте оглавление так, чтобы оно включало абзацы с заголовками уровней от 1 до 3.
// Также установите, чтобы его записи были гиперссылками, которые перенесут нас
// к месту заголовка при щелчке левой кнопкой мыши в Microsoft Word.
builder->InsertTableOfContents(u"\\o \"1-3\" \\h \\z \\u");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// Заполните оглавление, добавив абзацы со стилями заголовков.
// Каждый такой заголовок уровня от 1 до 3 создаст запись в оглавлении.
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"Heading 1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 1.1");
builder->Writeln(u"Heading 1.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"Heading 2");
builder->Writeln(u"Heading 3");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 3.1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading3);
builder->Writeln(u"Heading 3.1.1");
builder->Writeln(u"Heading 3.1.2");
builder->Writeln(u"Heading 3.1.3");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading4);
builder->Writeln(u"Heading 3.1.3.1");
builder->Writeln(u"Heading 3.1.3.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 3.2");
builder->Writeln(u"Heading 3.3");

// Оглавление — это поле типа, которое необходимо обновлять, чтобы отобразить актуальный результат.
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertToc.docx");
```


Показывает, как использовать поле QUOTE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте поле QUOTE, которое отобразит значение его свойства Text.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldQuote>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldQuote, true));
field->set_Text(u"\"Quoted text\"");

ASSERT_EQ(u" QUOTE  \"\\\"Quoted text\\\"\"", field->GetFieldCode());

// Вставьте поле QUOTE и вложите в него поле DATE.
// Поля DATE обновляют своё значение до текущей даты каждый раз, когда мы открываем документ в Microsoft Word.
// Вложение поля DATE в поле QUOTE таким образом заморозит его значение
// на дату, когда мы создали документ.
builder->Write(u"\nDocument creation date: ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldQuote>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldQuote, true));
builder->MoveTo(field->get_Separator());
builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true);

ASSERT_EQ(System::String(u" QUOTE \u0013 DATE \u0014") + System::DateTime::get_Now().get_Date().ToShortDateString() + u"\u0015", field->GetFieldCode());

// Обновите все поля, чтобы отобразить их правильные результаты.
doc->UpdateFields();

ASSERT_EQ(u"\"Quoted text\"", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.QUOTE.docx");
```


Показывает, как задать детали пользователя и отобразить их с помощью полей.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Создайте объект UserInformation и установите его в качестве источника данных для полей, отображающих информацию о пользователе.
auto userInformation = System::MakeObject<Aspose::Words::Fields::UserInformation>();
userInformation->set_Name(u"John Doe");
userInformation->set_Initials(u"J. D.");
userInformation->set_Address(u"123 Main Street");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

// Вставьте поля USERNAME, USERINITIALS и USERADDRESS, которые отображают значения
// соответствующих свойств объекта UserInformation, который мы создали выше.
ASSERT_EQ(userInformation->get_Name(), builder->InsertField(u" USERNAME ")->get_Result());
ASSERT_EQ(userInformation->get_Initials(), builder->InsertField(u" USERINITIALS ")->get_Result());
ASSERT_EQ(userInformation->get_Address(), builder->InsertField(u" USERADDRESS ")->get_Result());

// Объект параметров полей также имеет статического пользователя по умолчанию, к которому могут обращаться поля из всех документов.
Aspose::Words::Fields::UserInformation::get_DefaultUser()->set_Name(u"Default User");
Aspose::Words::Fields::UserInformation::get_DefaultUser()->set_Initials(u"D. U.");
Aspose::Words::Fields::UserInformation::get_DefaultUser()->set_Address(u"One Microsoft Way");
doc->get_FieldOptions()->set_CurrentUser(Aspose::Words::Fields::UserInformation::get_DefaultUser());

ASSERT_EQ(u"Default User", builder->InsertField(u" USERNAME ")->get_Result());
ASSERT_EQ(u"D. U.", builder->InsertField(u" USERINITIALS ")->get_Result());
ASSERT_EQ(u"One Microsoft Way", builder->InsertField(u" USERADDRESS ")->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"FieldOptions.CurrentUser.docx");
```

## См. также

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
