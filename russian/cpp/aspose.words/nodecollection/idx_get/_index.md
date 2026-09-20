---
title: "Aspose::Words::NodeCollection::idx_get метод"
linktitle: "idx_get"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::NodeCollection::idx_get метод. Получает узел по указанному индексу в C++."
type: docs
weight: 8000
url: /ru/cpp/aspose.words/nodecollection/idx_get/
---
## NodeCollection::idx_get method


Получает узел по заданному индексу.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::NodeCollection::idx_get(int32_t index)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int32_t | Индекс в коллекцию узлов. |
## Примечания


Индекс начинается с нуля.

Отрицательные индексы допускаются и указывают доступ с конца коллекции. Например, -1 означает последний элемент, -2 — предпоследний и так далее.

Если индекс больше или равен количеству элементов в списке, возвращается нулевая ссылка.

Если индекс отрицательный и его абсолютное значение больше количества элементов в списке, возвращается нулевая ссылка.

## Примеры



Показывает, как пройтись по коллекции дочерних узлов составного узла.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Добавьте два фрагмента текста и одну фигуру в качестве дочерних узлов к первому абзацу этого документа.
auto paragraph = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world! "));

auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(200);
shape->set_Height(200);
// Обратите внимание, что 'CustomNodeId' не сохраняется в выходной файл и существует только в течение жизни узла.
shape->set_CustomNodeId(100);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello again!"));

// Итерируйтесь по коллекции непосредственных дочерних элементов абзаца,
// и выводите любые фрагменты текста или фигуры, которые мы находим внутри.
System::SharedPtr<Aspose::Words::NodeCollection> children = paragraph->GetChildNodes(Aspose::Words::NodeType::Any, false);

ASSERT_EQ(3, paragraph->GetChildNodes(Aspose::Words::NodeType::Any, false)->get_Count());

for (auto&& child : System::IterateOver(children))
{
    switch (child->get_NodeType())
    {
        case Aspose::Words::NodeType::Run:
            std::cout << "Run contents:" << std::endl;
            std::cout << System::String::Format(u"\t\"{0}\"", child->GetText().Trim()) << std::endl;
            break;

        case Aspose::Words::NodeType::Shape:
        {
            auto childShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(child);
            std::cout << "Shape:" << std::endl;
            std::cout << System::String::Format(u"\t{0}, {1}x{2}", childShape->get_ShapeType(), childShape->get_Width(), childShape->get_Height()) << std::endl;
            ASSERT_EQ(100, shape->get_CustomNodeId());
            break;
        }

        default:
            break;
    }
}
```

## См. также

* Class [Node](../../node/)
* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
