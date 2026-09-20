---
title: "Класс Aspose::Words::Math::OfficeMath"
linktitle: "OfficeMath"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::Math::OfficeMath. Представляет объект Office Math, такой как функция, уравнение, матрица или аналогичный. Может содержать дочерние элементы, включая фрагменты математического текста, закладки, комментарии, другие экземпляры OfficeMath и некоторые другие узлы. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 1000
url: /ru/cpp/aspose.words.math/officemath/
---
## OfficeMath class


Представляет объект Office [Math](../), такой как функция, уравнение, матрица или аналогичный. Может содержать дочерние элементы, включая фрагменты математического текста, закладки, комментарии, другие экземпляры [OfficeMath](./) и некоторые другие узлы. Чтобы узнать больше, посетите статью документации [Working with OfficeMath](https://docs.aspose.com/words/cpp/working-with-officemath/).

```cpp
class OfficeMath : public Aspose::Words::CompositeNode,
                   public Aspose::Words::IInline,
                   public Aspose::Words::Revisions::ITrackableNode
```

## Методы

| Метод | Описание |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Принимает посетителя. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Принимает посетителя для посещения конца офисной математики. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Принимает посетителя для посещения начала офисной математики. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | Создаёт дубликат узла. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Возвращает количество непосредственных дочерних элементов этого узла. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Указывает пользовательский идентификатор узла. |
| [get_DisplayType](./get_displaytype/)() | Получает/устанавливает тип формата отображения Office [Math](../), который определяет, отображается ли уравнение inline с текстом или на отдельной строке. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Возвращает документ, к которому принадлежит этот узел. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Возвращает первого дочернего узла. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Возвращает **true**, если у этого узла есть дочерние узлы. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Возвращает **true**, поскольку этот узел может иметь дочерние узлы. |
| [get_Justification](./get_justification/)() | Получает/устанавливает выравнивание Office [Math](../). |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Возвращает последнего дочернего узла. |
| [get_MathObjectType](./get_mathobjecttype/)() const | Получает тип [MathObjectType](./get_mathobjecttype/) этого объекта Office [Math](../). |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Возвращает узел, непосредственно следующий за этим узлом. |
| [get_NodeType](./get_nodetype/)() const override | Возвращает [OfficeMath](../../aspose.words/nodetype/). |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Возвращает непосредственного родителя этого узла. |
| [get_ParentParagraph](./get_parentparagraph/)() | Получает родительский [Paragraph](../../aspose.words/paragraph/) этого узла. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Возвращает узел, непосредственно предшествующий этому узлу. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Возвращает объект [Range](../../aspose.words/range/), представляющий часть документа, содержащуюся в этом узле. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Возвращает первого предка указанного [NodeType](../../aspose.words/nodetype/). |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Возвращает N‑й дочерний узел, соответствующий указанному типу. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Возвращает живую коллекцию дочерних узлов, соответствующих указанному типу. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | Обеспечивает поддержку итерации в стиле foreach по дочерним узлам этого узла. |
| [GetMathRenderer](./getmathrenderer/)() | Создаёт и возвращает объект, который можно использовать для рендеринга этого уравнения в изображение. |
| [GetText](../../aspose.words/compositenode/gettext/)() override | Получает текст этого узла и всех его дочерних узлов. |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../../aspose.words/compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Возвращает индекс указанного дочернего узла в массиве дочерних узлов. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Получает следующий узел согласно алгоритму обхода дерева в порядке предобхода. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | Вспомогательный метод, преобразующий значение перечисления типа узла в удобочитаемую строку. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Получает предыдущий узел согласно алгоритму обхода дерева в порядке предобхода. |
| [Remove](../../aspose.words/node/remove/)() | Удаляет себя из родительского узла. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Удаляет все дочерние узлы текущего узла. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Удаляет все дочерние узлы [SmartTag](../../aspose.words.markup/smarttag/) текущего узла. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(const System::String\&) | Выбирает список узлов, соответствующих XPath-выражению. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(const System::String\&) | Выбирает первый [Node](../../aspose.words/node/), соответствующий XPath-выражению. |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Сеттер для [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_DisplayType](./set_displaytype/)(Aspose::Words::Math::OfficeMathDisplayType) | Сеттер для [Aspose::Words::Math::OfficeMath::get_DisplayType](./get_displaytype/). |
| [set_Justification](./set_justification/)(Aspose::Words::Math::OfficeMathJustification) | Сеттер для [Aspose::Words::Math::OfficeMath::get_Justification](./get_justification/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Экспортирует содержимое узла в строку в указанном формате. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |
| static [Type](./type/)() |  |
## Примечания


В этой версии Aspose.Words узлы [OfficeMath](./) не предоставляют публичных методов и свойств для создания или изменения объекта [OfficeMath](./). В этой версии вы не можете создавать узлы [Math](../) или изменять существующие, кроме их удаления.

[OfficeMath](./) can only be a child of [Paragraph](../../aspose.words/paragraph/).

## Примеры



Показывает, как задать формат отображения офисной математики.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto officeMath = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));

// Узлы OfficeMath, являющиеся дочерними для других узлов OfficeMath, всегда inline.
// Узел, с которым мы работаем, является базовым узлом для изменения его расположения и типа отображения.
ASSERT_EQ(Aspose::Words::Math::MathObjectType::OMathPara, officeMath->get_MathObjectType());
ASSERT_EQ(Aspose::Words::NodeType::OfficeMath, officeMath->get_NodeType());
ASPOSE_ASSERT_EQ(officeMath->get_ParentNode(), officeMath->get_ParentParagraph());

// Измените расположение и тип отображения узла OfficeMath.
officeMath->set_DisplayType(Aspose::Words::Math::OfficeMathDisplayType::Display);
officeMath->set_Justification(Aspose::Words::Math::OfficeMathJustification::Left);

doc->Save(get_ArtifactsDir() + u"Shape.OfficeMath.docx");
```

## См. также

* Class [CompositeNode](../../aspose.words/compositenode/)
* Namespace [Aspose::Words::Math](../)
* Library [Aspose.Words for C++](../../)
