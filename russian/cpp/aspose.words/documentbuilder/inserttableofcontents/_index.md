---
title: "Aspose::Words::DocumentBuilder::InsertTableOfContents method"
linktitle: "InsertTableOfContents"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::DocumentBuilder::InsertTableOfContents method. Вставляет поле TOC (таблица содержимого) в документ на C++."
type: docs
weight: 48000
url: /ru/cpp/aspose.words/documentbuilder/inserttableofcontents/
---
## DocumentBuilder::InsertTableOfContents method


Вставляет поле TOC (оглавление) в документ.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::DocumentBuilder::InsertTableOfContents(const System::String &switches)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| переключатели | const System::String\& | Переключатели поля TOC. |
## Примечания


Этот метод вставляет поле TOC (таблица содержимого) в документ в текущей позиции.

Таблица содержимого в документе Word может быть построена различными способами и отформатирована с использованием множества параметров. Способ построения и отображения таблицы в Microsoft Word контролируется переключателями поля.

Самый простой способ задать переключатели — вставить и настроить таблицу содержимого в документ Word, используя меню Insert->Reference->Index и [Tables](../../../aspose.words.tables/) меню, затем включить отображение кодов полей, чтобы увидеть переключатели. Вы можете нажать Alt+F9 в Microsoft Word, чтобы включать или отключать отображение кодов полей.

Например, после создания таблицы содержимого в документ вставляется следующее поле: **%{ TOC \o "1-3" \h \z }**. Вы можете скопировать **%\o "1-3" \h \z** и использовать его в качестве параметра переключателей.

Обратите внимание, что [InsertTableOfContents()](../) только вставит поле TOC, но фактически не построит таблицу содержимого. Таблица содержимого создаётся Microsoft Word при обновлении поля.

Если вы вставите таблицу содержимого с помощью этого метода и затем откроете файл в Microsoft Word, вы не увидите таблицу содержимого, потому что поле TOC ещё не обновлено.

В Microsoft Word поля не обновляются автоматически при открытии документа, но вы можете обновить поля в любой момент, нажав F9.

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

## См. также

* Class [Field](../../../aspose.words.fields/field/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
