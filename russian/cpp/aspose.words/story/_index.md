---
title: "Aspose::Words::Story class"
linktitle: "Story"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Story class. Базовый класс для элементов, содержащих блочные узлы Paragraph и Table. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 63000
url: /ru/cpp/aspose.words/story/
---
## Story class


Базовый класс для элементов, содержащих блочные узлы [Paragraph](../paragraph/) и [Table](../../aspose.words.tables/table/). Чтобы узнать больше, посетите статью документации [Logical Levels of Nodes in a Document](https://docs.aspose.com/words/cpp/logical-levels-of-nodes-in-a-document/).

```cpp
class Story : public Aspose::Words::CompositeNode,
              public Aspose::Words::IStory
```

## Методы

| Метод | Описание |
| --- | --- |
| virtual [Accept](../node/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Принимает посетителя. |
| virtual [AcceptEnd](../compositenode/acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Когда реализовано в производном классе, вызывает метод VisitXXXEnd указанного посетителя документа. |
| virtual [AcceptStart](../compositenode/acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Когда реализовано в производном классе, вызывает метод VisitXXXStart указанного посетителя документа. |
| [AppendChild](../compositenode/appendchild/)(T) |  |
| [AppendParagraph](./appendparagraph/)(const System::String\&) | Метод‑ярлык, который создает объект [Paragraph](../paragraph/) с необязательным текстом и добавляет его в конец этого объекта. |
| [Clone](../node/clone/)(bool) | Создаёт дубликат узла. |
| [DeleteShapes](./deleteshapes/)() | Удаляет все фигуры из текста этой истории. |
| [get_Count](../compositenode/get_count/)() | Возвращает количество непосредственных дочерних элементов этого узла. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Указывает пользовательский идентификатор узла. |
| virtual [get_Document](../node/get_document/)() const | Возвращает документ, к которому принадлежит этот узел. |
| [get_FirstChild](../compositenode/get_firstchild/)() const | Возвращает первого дочернего узла. |
| [get_FirstParagraph](./get_firstparagraph/)() override | Возвращает первый абзац в истории. |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | Возвращает **true**, если у этого узла есть дочерние узлы. |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | Возвращает **true**, поскольку этот узел может иметь дочерние узлы. |
| [get_LastChild](../compositenode/get_lastchild/)() const | Возвращает последнего дочернего узла. |
| [get_LastParagraph](./get_lastparagraph/)() override | Возвращает последний абзац в истории. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Возвращает узел, непосредственно следующий за этим узлом. |
| virtual [get_NodeType](../node/get_nodetype/)() const | Возвращает тип этого узла. |
| [get_Paragraphs](./get_paragraphs/)() override | Возвращает коллекцию абзацев, которые являются непосредственными дочерними элементами истории. |
| [get_ParentNode](../node/get_parentnode/)() | Возвращает непосредственного родителя этого узла. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Возвращает узел, непосредственно предшествующий этому узлу. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Возвращает объект [Range](../range/), представляющий часть документа, содержащуюся в этом узле. |
| [get_StoryType](./get_storytype/)() override | Возвращает тип этой истории. |
| [get_Tables](./get_tables/)() override | Возвращает коллекцию таблиц, которые являются непосредственными дочерними элементами истории. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Получает первого предка указанного [NodeType](../nodetype/). |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetChild](../compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Возвращает N‑й дочерний узел, соответствующий указанному типу. |
| [GetChildNodes](../compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Возвращает живую коллекцию дочерних узлов, соответствующих указанному типу. |
| [GetEnumerator](../compositenode/getenumerator/)() override | Обеспечивает поддержку итерации в стиле foreach по дочерним узлам этого узла. |
| [GetText](../compositenode/gettext/)() override | Получает текст этого узла и всех его дочерних узлов. |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Возвращает индекс указанного дочернего узла в массиве дочерних узлов. |
| [InsertAfter](../compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Получает следующий узел согласно алгоритму обхода дерева в порядке предобхода. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | Вспомогательный метод, преобразующий значение перечисления типа узла в удобочитаемую строку. |
| [PrependChild](../compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Получает предыдущий узел согласно алгоритму обхода дерева в порядке предобхода. |
| [Remove](../node/remove/)() | Удаляет себя из родительского узла. |
| [RemoveAllChildren](../compositenode/removeallchildren/)() | Удаляет все дочерние узлы текущего узла. |
| [RemoveChild](../compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../compositenode/removesmarttags/)() | Удаляет все дочерние узлы [SmartTag](../../aspose.words.markup/smarttag/) текущего узла. |
| [SelectNodes](../compositenode/selectnodes/)(const System::String\&) | Выбирает список узлов, соответствующих XPath-выражению. |
| [SelectSingleNode](../compositenode/selectsinglenode/)(const System::String\&) | Выбирает первый [Node](../node/), который соответствует выражению XPath. |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Сеттер для [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Экспортирует содержимое узла в строку в указанном формате. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |
| static [Type](./type/)() |  |
## Примечания


Текст документа Word считается состоящим из нескольких историй. Основной текст хранится в основной истории текста, представленной [Body](../body/), каждый верхний и нижний колонтитул хранится в отдельной истории, представленной [HeaderFooter](../headerfooter/).

## Примеры



Показывает, как удалить все фигуры из узла.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Используйте DocumentBuilder для вставки фигуры. Это встроенная фигура,
// которая имеет родительский Paragraph, являющийся дочерним узлом Body первой секции.
builder->InsertShape(Aspose::Words::Drawing::ShapeType::Cube, 100.0, 100.0);

ASSERT_EQ(1, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());

// Мы можем удалить все фигуры из дочерних абзацев этого Body.
ASSERT_EQ(Aspose::Words::StoryType::MainText, doc->get_FirstSection()->get_Body()->get_StoryType());
doc->get_FirstSection()->get_Body()->DeleteShapes();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
```

## См. также

* Class [CompositeNode](../compositenode/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
