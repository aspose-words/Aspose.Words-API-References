---
title: "Aspose::Words::Body класс"
linktitle: "Body"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Body class. Представляет контейнер для основного текста раздела. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words/body/
---
## Body class


Представляет контейнер для основного текста раздела. Чтобы узнать больше, посетите статью документации [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class Body : public Aspose::Words::Story
```

## Методы

| Метод | Описание |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Принимает посетителя. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Принимает посетителя для посещения конца тела документа. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Принимает посетителя для посещения начала тела документа. |
| [AppendChild](../compositenode/appendchild/)(T) |  |
| [AppendParagraph](../story/appendparagraph/)(const System::String\&) | Метод‑ярлык, который создает объект [Paragraph](../paragraph/) с необязательным текстом и добавляет его в конец этого объекта. |
| [Body](./body/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) | Инициализирует новый экземпляр класса [Body](./). |
| [Clone](../node/clone/)(bool) | Создаёт дубликат узла. |
| [DeleteShapes](../story/deleteshapes/)() | Удаляет все фигуры из текста этой истории. |
| [EnsureMinimum](./ensureminimum/)() | Если последний дочерний элемент не является абзацем, создаёт и добавляет один пустой абзац. |
| [get_Count](../compositenode/get_count/)() | Возвращает количество непосредственных дочерних элементов этого узла. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Указывает пользовательский идентификатор узла. |
| virtual [get_Document](../node/get_document/)() const | Возвращает документ, к которому принадлежит этот узел. |
| [get_FirstChild](../compositenode/get_firstchild/)() const | Возвращает первого дочернего узла. |
| [get_FirstParagraph](../story/get_firstparagraph/)() override | Возвращает первый абзац в истории. |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | Возвращает **true**, если у этого узла есть дочерние узлы. |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | Возвращает **true**, поскольку этот узел может иметь дочерние узлы. |
| [get_LastChild](../compositenode/get_lastchild/)() const | Возвращает последнего дочернего узла. |
| [get_LastParagraph](../story/get_lastparagraph/)() override | Возвращает последний абзац в истории. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Возвращает узел, непосредственно следующий за этим узлом. |
| [get_NodeType](./get_nodetype/)() const override | Возвращает [Body](../nodetype/). |
| [get_Paragraphs](../story/get_paragraphs/)() override | Возвращает коллекцию абзацев, которые являются непосредственными дочерними элементами истории. |
| [get_ParentNode](../node/get_parentnode/)() | Возвращает непосредственного родителя этого узла. |
| [get_ParentSection](./get_parentsection/)() | Получает родительский раздел этой истории. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Возвращает узел, непосредственно предшествующий этому узлу. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Возвращает объект [Range](../range/), представляющий часть документа, содержащуюся в этом узле. |
| [get_StoryType](../story/get_storytype/)() override | Возвращает тип этой истории. |
| [get_Tables](../story/get_tables/)() override | Возвращает коллекцию таблиц, которые являются непосредственными дочерними элементами истории. |
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


[Body](./) can contain [Paragraph](../paragraph/) and [Table](../../aspose.words.tables/table/) child nodes.

[Body](./) is a section-level node and can only be a child of [Section](../section/). There can only be one [Body](./) in a [Section](../section/).

Минимальный корректный [Body](./) должен содержать как минимум один [Paragraph](../paragraph/).

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

* Class [Story](../story/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
