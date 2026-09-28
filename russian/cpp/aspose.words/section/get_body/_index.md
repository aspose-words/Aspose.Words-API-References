---
title: "Aspose::Words::Section::get_Body метод"
linktitle: "get_Body"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Section::get_Body метод. Возвращает дочерний узел Body раздела в C++."
type: docs
weight: 10000
url: /ru/cpp/aspose.words/section/get_body/
---
## Section::get_Body method


Возвращает дочерний узел [Body](../../body/) раздела.

```cpp
System::SharedPtr<Aspose::Words::Body> Aspose::Words::Section::get_Body()
```

## Примечания


[Body](../../body/) contains main text of the section.

Возвращает **null**, если у раздела нет узла [Body](../../body/) среди его дочерних элементов.

## Примеры



Очищает основной текст во всех разделах документа, оставляя сами разделы.
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

// Разделу требуется тело, которое будет содержать и отображать всё его содержимое
// на странице между заголовком и нижним колонтитулом раздела.
auto body = System::MakeObject<Aspose::Words::Body>(doc);
section->AppendChild<System::SharedPtr<Aspose::Words::Body>>(body);

// У этого тела нет дочерних элементов, поэтому пока нельзя добавить в него run.
ASSERT_EQ(0, doc->get_FirstSection()->get_Body()->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Вызовите "EnsureMinimum", чтобы убедиться, что это тело содержит хотя бы один пустой абзац.
body->EnsureMinimum();

// Теперь мы можем добавить run в тело и заставить документ отобразить их.
body->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## См. также

* Class [Body](../../body/)
* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
