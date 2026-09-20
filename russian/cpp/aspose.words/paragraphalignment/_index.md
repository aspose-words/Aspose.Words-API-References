---
title: "Aspose::Words::ParagraphAlignment enum"
linktitle: "ParagraphAlignment"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::ParagraphAlignment enum. Указывает выравнивание текста в абзаце в C++."
type: docs
weight: 110000
url: /ru/cpp/aspose.words/paragraphalignment/
---
## ParagraphAlignment enum


Указывает выравнивание текста в абзаце.

```cpp
enum class ParagraphAlignment
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Слева | 0 | Текст выровнен по левому краю. |
| По центру | 1 | Текст центрирован по горизонтали. |
| Справа | 2 | Текст выровнен по правому краю. |
| Выравнивание | 3 | Текст выровнен по левому и правому краю. |
| Distributed | 4 | Текст равномерно распределён. |
| ArabicMediumKashida | 5 | Только арабский. Длина кашиды в тексте увеличивается до средней длины, определяемой потребителем. |
| ArabicHighKashida | 7 | Только арабский. Длина кашиды в тексте увеличивается до максимально возможной длины. |
| ArabicLowKashida | 8 | Только арабский. Длина кашиды в тексте увеличивается до слегка более длинной длины. |
| ThaiDistributed | 9 | Только тайский. Текст выравнивается по ширине с оптимизацией для тайского языка. |
| MathElementCenterAsGroup | 10 | Единственный элемент [Math](../../aspose.words.math/) в строке, выровненный как 'Centered As Group'. |


## Примеры



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
