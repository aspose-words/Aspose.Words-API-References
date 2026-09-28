---
title: "Aspose::Words::Node::GetText method"
linktitle: "GetText"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Node::GetText method. Получает текст этого узла и всех его дочерних узлов в C++."
type: docs
weight: 15000
url: /ru/cpp/aspose.words/node/gettext/
---
## Node::GetText method


Получает текст этого узла и всех его дочерних узлов.

```cpp
virtual System::String Aspose::Words::Node::GetText()
```

## Примечания


Возвращаемая строка включает все управляющие и специальные символы, как описано в [ControlChar](../../controlchar/).

## Примеры



Показывает, как использовать управляющие символы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставка абзацев с текстом с помощью DocumentBuilder.
builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

// Преобразование документа в текстовый вид показывает, что управляющие символы
// представляют некоторые структурные элементы документа, такие как разрывы страниц.
ASSERT_EQ(System::String::Format(u"Hello world!{0}", Aspose::Words::ControlChar::Cr()) + System::String::Format(u"Hello again!{0}", Aspose::Words::ControlChar::Cr()) + Aspose::Words::ControlChar::PageBreak(), doc->GetText());

// При преобразовании документа в строковый вид,
// мы можем опустить некоторые управляющие символы с помощью метода Trim.
ASSERT_EQ(System::String::Format(u"Hello world!{0}", Aspose::Words::ControlChar::Cr()) + u"Hello again!", doc->GetText().Trim());
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

* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
