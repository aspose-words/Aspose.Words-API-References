---
title: "Метод Aspose::Words::ParagraphFormat::get_StyleIdentifier"
linktitle: "get_StyleIdentifier"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::ParagraphFormat::get_StyleIdentifier. Получает или задаёт независимый от локали идентификатор стиля абзаца, применяемый к этому форматированию в C++."
type: docs
weight: 36000
url: /ru/cpp/aspose.words/paragraphformat/get_styleidentifier/
---
## ParagraphFormat::get_StyleIdentifier method


Получает или задает независимый от локали идентификатор стиля абзаца, применяемый к этому форматированию.

```cpp
Aspose::Words::StyleIdentifier Aspose::Words::ParagraphFormat::get_StyleIdentifier()
```


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

* Enum [StyleIdentifier](../../styleidentifier/)
* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
