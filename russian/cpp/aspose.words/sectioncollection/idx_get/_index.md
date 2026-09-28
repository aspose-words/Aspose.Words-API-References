---
title: "Aspose::Words::SectionCollection::idx_get метод"
linktitle: "idx_get"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::SectionCollection::idx_get метод. Получает раздел по указанному индексу в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words/sectioncollection/idx_get/
---
## SectionCollection::idx_get method


Получает раздел по заданному индексу.

```cpp
System::SharedPtr<Aspose::Words::Section> Aspose::Words::SectionCollection::idx_get(int32_t index)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int32_t | Индекс в списке разделов. |
## Примечания


Индекс начинается с нуля.

Отрицательные индексы допускаются и указывают доступ с конца коллекции. Например, -1 означает последний элемент, -2 — предпоследний и так далее.

Если индекс больше или равен количеству элементов в списке, возвращается нулевая ссылка.

Если индекс отрицательный и его абсолютное значение больше количества элементов в списке, возвращается нулевая ссылка.

## Примеры



Показывает, когда необходимо пересчитать макет страниц документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Сохранение документа в PDF, в изображение или печать в первый раз будет автоматически
// кешировать макет документа в его страницах.
doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.1.pdf");

// Измените документ каким-либо образом.
doc->get_Styles()->idx_get(u"Normal")->get_Font()->set_Size(6);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Margins(Aspose::Words::Margins::Mirrored);

// В текущей версии Aspose.Words изменение документа не приводит к автоматическому пересозданию
// кешированный макет страницы. Если мы хотим, чтобы кешированный макет
// чтобы оставаться актуальным, нам придётся обновлять его вручную.
doc->UpdatePageLayout();

doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.2.pdf");
```


Показывает, как подготовить новый узел раздела для редактирования.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Пустой документ содержит раздел, у которого есть тело, которое, в свою очередь, имеет абзац.
// Мы можем добавить содержимое в этот документ, добавляя такие элементы, как текстовые фрагменты, фигуры или таблицы, в этот абзац.
ASSERT_EQ(Aspose::Words::NodeType::Section, doc->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Body, doc->get_Sections()->idx_get(0)->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, doc->get_Sections()->idx_get(0)->get_Body()->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());

// Если мы добавим новый раздел таким образом, у него не будет тела или каких-либо других дочерних узлов.
doc->get_Sections()->Add(System::MakeObject<Aspose::Words::Section>(doc));

ASSERT_EQ(0, doc->get_Sections()->idx_get(1)->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Выполните метод "EnsureMinimum", чтобы добавить тело и абзац в этот раздел и начать его редактирование.
doc->get_LastSection()->EnsureMinimum();

ASSERT_EQ(Aspose::Words::NodeType::Body, doc->get_Sections()->idx_get(1)->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, doc->get_Sections()->idx_get(1)->get_Body()->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());

doc->get_Sections()->idx_get(0)->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## См. также

* Class [Section](../../section/)
* Class [SectionCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
