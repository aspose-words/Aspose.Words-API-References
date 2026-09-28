---
title: "класс Aspose::Words::Node"
linktitle: "Node"
second_title: "Справочник API Aspose.Words для C++"
description: "класс Aspose::Words::Node. Базовый класс для всех узлов документа Word. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 41000
url: /ru/cpp/aspose.words/node/
---
## Node class


Базовый класс для всех узлов Word‑документа. Чтобы узнать больше, посетите статью документации [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class Node : public virtual System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| virtual [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Принимает посетителя. |
| [Clone](./clone/)(bool) | Создаёт дубликат узла. |
| [get_CustomNodeId](./get_customnodeid/)() const | Указывает пользовательский идентификатор узла. |
| virtual [get_Document](./get_document/)() const | Возвращает документ, к которому принадлежит этот узел. |
| virtual [get_IsComposite](./get_iscomposite/)() | Возвращает **true**, если этот узел может содержать другие узлы. |
| [get_NextNode](./get_nextnode/)() const |  |
| [get_NextSibling](./get_nextsibling/)() | Возвращает узел, непосредственно следующий за этим узлом. |
| virtual [get_NodeType](./get_nodetype/)() const | Возвращает тип этого узла. |
| [get_ParentNode](./get_parentnode/)() | Возвращает непосредственного родителя этого узла. |
| [get_PreviousSibling](./get_previoussibling/)() | Возвращает узел, непосредственно предшествующий этому узлу. |
| [get_PrevNode](./get_prevnode/)() const |  |
| [get_Range](./get_range/)() | Возвращает объект [Range](../range/), представляющий часть документа, содержащуюся в этом узле. |
| [GetAncestor](./getancestor/)(Aspose::Words::NodeType) | Получает первого предка указанного [NodeType](../nodetype/). |
| [GetAncestorOf](./getancestorof/)() |  |
| virtual [GetText](./gettext/)() | Получает текст этого узла и всех его дочерних узлов. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](./isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](./nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Получает следующий узел согласно алгоритму обхода дерева в порядке предобхода. |
| static [NodeTypeToString](./nodetypetostring/)(Aspose::Words::NodeType) | Вспомогательный метод, преобразующий значение перечисления типа узла в удобочитаемую строку. |
| [PreviousPreOrder](./previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Получает предыдущий узел согласно алгоритму обхода дерева в порядке предобхода. |
| [Remove](./remove/)() | Удаляет себя из родительского узла. |
| [set_CustomNodeId](./set_customnodeid/)(int32_t) | Сеттер для [Aspose::Words::Node::get_CustomNodeId](./get_customnodeid/). |
| [set_NextNode](./set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](./set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](./setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [ToString](./tostring/)(Aspose::Words::SaveFormat) | Экспортирует содержимое узла в строку в указанном формате. |
| [ToString](./tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |
| static [Type](./type/)() |  |
## Примечания


Документ представляется в виде дерева узлов, похожего на DOM или XmlDocument.

Для получения дополнительной информации см. шаблон проектирования Composite.

Класс [Node](./):

* Defines the child node interface.
* Defines the interface for visiting nodes.
* Provides default cloning capability.
* Implements parent node and owner document mechanisms.
* Implements access to sibling nodes.



## Примеры



Показывает, как клонировать составной узел.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

// Ниже представлены два способа клонирования составного узла.
// 1 -  Создать клон узла и также создать клон каждого из его дочерних узлов.
System::SharedPtr<Aspose::Words::Node> cloneWithChildren = System::ExplicitCast<Aspose::Words::Node>(para)->Clone(true);

ASSERT_TRUE((System::ExplicitCast<Aspose::Words::CompositeNode>(cloneWithChildren))->get_HasChildNodes());
ASSERT_EQ(u"Hello world!", cloneWithChildren->GetText().Trim());

// 2 -  Создать клон узла только самого себя без каких-либо дочерних узлов.
System::SharedPtr<Aspose::Words::Node> cloneWithoutChildren = System::ExplicitCast<Aspose::Words::Node>(para)->Clone(false);

ASSERT_FALSE((System::ExplicitCast<Aspose::Words::CompositeNode>(cloneWithoutChildren))->get_HasChildNodes());
ASSERT_EQ(System::String::Empty, cloneWithoutChildren->GetText().Trim());
```


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


Показывает, как удалить все дочерние узлы определённого типа из составного узла.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

ASSERT_EQ(2, doc->GetChildNodes(Aspose::Words::NodeType::Table, true)->get_Count());

System::SharedPtr<Aspose::Words::Node> curNode = doc->get_FirstSection()->get_Body()->get_FirstChild();

while (curNode != nullptr)
{
    // Сохраните следующий соседний узел в переменную на случай, если нам понадобится перейти к нему после удаления текущего узла.
    System::SharedPtr<Aspose::Words::Node> nextNode = curNode->get_NextSibling();

    // Тело раздела может содержать узлы Paragraph и Table.
    // Если узел является таблицей, удалите его из родителя.
    if (curNode->get_NodeType() == Aspose::Words::NodeType::Table)
    {
        curNode->Remove();
    }

    curNode = nextNode;
}

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Table, true)->get_Count());
```

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
