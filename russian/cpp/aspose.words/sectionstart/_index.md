---
title: "Aspose::Words::SectionStart enum"
linktitle: "SectionStart"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::SectionStart enum. Тип разрыва в начале раздела в C++."
type: docs
weight: 116000
url: /ru/cpp/aspose.words/sectionstart/
---
## SectionStart enum


Тип разрыва в начале раздела.

```cpp
enum class SectionStart
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Continuous | 0 | Новый раздел начинается на той же странице, что и предыдущий раздел. |
| NewColumn | 1 | Раздел начинается с новой колонки. |
| NewPage | 2 | Раздел начинается с новой страницы. |
| EvenPage | 3 | Раздел начинается на новой четной странице. |
| OddPage | 4 | Раздел начинается на новой нечетной странице. |


## Примеры



Показывает, как указать, как новый раздел отделяется от предыдущего.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"This text is in section 1.");

// Типы разрывов разделов определяют, как новый раздел отделяется от предыдущего раздела.
// Ниже представлены пять типов разрывов разделов.
// 1 -  Начинает следующий раздел на новой странице:
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Writeln(u"This text is in section 2.");

ASSERT_EQ(Aspose::Words::SectionStart::NewPage, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_SectionStart());

// 2 -  Начинает следующий раздел на текущей странице:
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakContinuous);
builder->Writeln(u"This text is in section 3.");

ASSERT_EQ(Aspose::Words::SectionStart::Continuous, doc->get_Sections()->idx_get(2)->get_PageSetup()->get_SectionStart());

// 3 -  Начинает следующий раздел на новой чётной странице:
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakEvenPage);
builder->Writeln(u"This text is in section 4.");

ASSERT_EQ(Aspose::Words::SectionStart::EvenPage, doc->get_Sections()->idx_get(3)->get_PageSetup()->get_SectionStart());

// 4 -  Начинает следующий раздел на новой нечётной странице:
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakOddPage);
builder->Writeln(u"This text is in section 5.");

ASSERT_EQ(Aspose::Words::SectionStart::OddPage, doc->get_Sections()->idx_get(4)->get_PageSetup()->get_SectionStart());

// 5 -  Начинает следующий раздел в новой колонке:
System::SharedPtr<Aspose::Words::TextColumnCollection> columns = builder->get_PageSetup()->get_TextColumns();
columns->SetCount(2);

builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewColumn);
builder->Writeln(u"This text is in section 6.");

ASSERT_EQ(Aspose::Words::SectionStart::NewColumn, doc->get_Sections()->idx_get(5)->get_PageSetup()->get_SectionStart());

doc->Save(get_ArtifactsDir() + u"PageSetup.SetSectionStart.docx");
```


Показывает, как вручную построить документ Aspose.Words.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Пустой документ содержит один раздел, одно тело и один абзац.
// Вызовите метод "RemoveAllChildren", чтобы удалить все эти узлы,
// и в результате получите узел документа без дочерних элементов.
doc->RemoveAllChildren();

// У этого документа теперь нет составных дочерних узлов, к которым мы могли бы добавить содержимое.
// Если мы захотим отредактировать его, нам потребуется заново заполнить его коллекцию узлов.
// Сначала создайте новый раздел, а затем добавьте его как дочерний элемент к корневому узлу документа.
auto section = System::MakeObject<Aspose::Words::Section>(doc);
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(section);

// Установите некоторые свойства разметки страницы для раздела.
section->get_PageSetup()->set_SectionStart(Aspose::Words::SectionStart::NewPage);
section->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Letter);

// Разделу требуется тело, которое будет содержать и отображать всё его содержимое
// на странице между заголовком и нижним колонтитулом раздела.
auto body = System::MakeObject<Aspose::Words::Body>(doc);
section->AppendChild<System::SharedPtr<Aspose::Words::Body>>(body);

// Создайте абзац, задайте некоторые свойства форматирования и затем добавьте его как дочерний элемент к телу.
auto para = System::MakeObject<Aspose::Words::Paragraph>(doc);

para->get_ParagraphFormat()->set_StyleName(u"Heading 1");
para->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

body->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(para);

// Наконец, добавьте некоторое содержимое в документ. Создайте объект Run,
// задайте его внешний вид и содержимое, а затем добавьте его как дочерний элемент к абзацу.
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"Hello World!");
run->get_Font()->set_Color(System::Drawing::Color::get_Red());
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

ASSERT_EQ(u"Hello World!", doc->GetText().Trim());

doc->Save(get_ArtifactsDir() + u"Section.CreateManually.docx");
```

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
