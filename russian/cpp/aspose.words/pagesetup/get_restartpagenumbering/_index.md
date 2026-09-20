---
title: "Метод Aspose::Words::PageSetup::get_RestartPageNumbering"
linktitle: "get_RestartPageNumbering"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::PageSetup::get_RestartPageNumbering. Истина, если нумерация страниц начинается заново в начале раздела в C++."
type: docs
weight: 38000
url: /ru/cpp/aspose.words/pagesetup/get_restartpagenumbering/
---
## PageSetup::get_RestartPageNumbering method


True, если нумерация страниц начинается заново в начале раздела.

```cpp
bool Aspose::Words::PageSetup::get_RestartPageNumbering()
```


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

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
