---
title: "Aspose::Words::PaperSize enum"
linktitle: "PaperSize"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::PaperSize enum. Указывает размер бумаги в C++."
type: docs
weight: 109000
url: /ru/cpp/aspose.words/papersize/
---
## PaperSize enum


Указывает размер бумаги.

```cpp
enum class PaperSize
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| A3 | 0 | 297 x 420 mm. |
| A4 | 1 | 210 x 297 mm. |
| A5 | 2 | 148 x 210 mm. |
| B4 | 3 | 250 x 353 mm. |
| B5 | 4 | 176 x 250 mm. |
| Executive | 5 | 7.25 x 10.5 дюйма. |
| Folio | 6 | 8.5 x 13 дюймов. |
| Ledger | 7 | 17 x 11 дюймов. |
| Legal | 8 | 8.5 x 14 дюймов. |
| Letter | 9 | 8.5 x 11 дюймов. |
| EnvelopeDL | 10 | 110 x 220 mm. |
| Quarto | 11 | 8.47 x 10.83 inches. |
| Statement | 12 | 8.5 x 5.5 inches. |
| Tabloid | 13 | 11 x 17 inches. |
| Paper10x14 | 14 | 10 x 14 inches. |
| Paper11x17 | 15 | 11 x 17 inches. |
| Number10Envelope | 16 | 4.125 x 9.5 inches. |
| JisB4 | 17 | 257 x 364 mm. |
| JisB5 | 18 | 182 x 257 mm. |
| Пользовательский | 19 | Пользовательский размер бумаги. |


## Примеры



Показывает, как настроить размер бумаги, ориентацию, поля и другие параметры раздела.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Legal);
builder->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
builder->get_PageSetup()->set_TopMargin(Aspose::Words::ConvertUtil::InchToPoint(1.0));
builder->get_PageSetup()->set_BottomMargin(Aspose::Words::ConvertUtil::InchToPoint(1.0));
builder->get_PageSetup()->set_LeftMargin(Aspose::Words::ConvertUtil::InchToPoint(1.5));
builder->get_PageSetup()->set_RightMargin(Aspose::Words::ConvertUtil::InchToPoint(1.5));
builder->get_PageSetup()->set_HeaderDistance(Aspose::Words::ConvertUtil::InchToPoint(0.2));
builder->get_PageSetup()->set_FooterDistance(Aspose::Words::ConvertUtil::InchToPoint(0.2));

builder->Writeln(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"PageSetup.PageMargins.docx");
```


Показывает, как установить размеры страниц.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Мы можем изменить размер текущей страницы на предопределённый размер
// используя свойство "PaperSize" объекта PageSetup этого раздела.
builder->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Tabloid);

ASPOSE_ASSERT_EQ(792.0, builder->get_PageSetup()->get_PageWidth());
ASPOSE_ASSERT_EQ(1224.0, builder->get_PageSetup()->get_PageHeight());

builder->Writeln(System::String::Format(u"This page is {0}x{1}.", builder->get_PageSetup()->get_PageWidth(), builder->get_PageSetup()->get_PageHeight()));

// Каждый раздел имеет свой собственный объект PageSetup. Когда мы используем построитель документа для создания нового раздела,
// объект PageSetup этого раздела наследует все значения объекта PageSetup предыдущего раздела.
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakEvenPage);

ASSERT_EQ(Aspose::Words::PaperSize::Tabloid, builder->get_PageSetup()->get_PaperSize());

builder->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::A5);
builder->Writeln(System::String::Format(u"This page is {0}x{1}.", builder->get_PageSetup()->get_PageWidth(), builder->get_PageSetup()->get_PageHeight()));

ASPOSE_ASSERT_EQ(419.55, builder->get_PageSetup()->get_PageWidth());
ASPOSE_ASSERT_EQ(595.30, builder->get_PageSetup()->get_PageHeight());

builder->InsertBreak(Aspose::Words::BreakType::SectionBreakEvenPage);

// Установите пользовательский размер для страниц этого раздела.
builder->get_PageSetup()->set_PageWidth(620);
builder->get_PageSetup()->set_PageHeight(480);

ASSERT_EQ(Aspose::Words::PaperSize::Custom, builder->get_PageSetup()->get_PaperSize());

builder->Writeln(System::String::Format(u"This page is {0}x{1}.", builder->get_PageSetup()->get_PageWidth(), builder->get_PageSetup()->get_PageHeight()));

doc->Save(get_ArtifactsDir() + u"PageSetup.PaperSizes.docx");
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
