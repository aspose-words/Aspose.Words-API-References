---
title: "Aspose::Words::Inline class"
linktitle: "Встроенный"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::Inline. Базовый класс для узлов уровня inline, которые могут иметь связанную с ними символьную форматировку, но не могут иметь дочерних узлов. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 36000
url: /ru/cpp/aspose.words/inline/
---
## Inline class


Базовый класс для узлов уровня inline, которые могут иметь связанную с ними символьную форматировку, но не могут иметь собственных дочерних узлов. Чтобы узнать больше, посетите статью документации [Logical Levels of Nodes in a Document](https://docs.aspose.com/words/cpp/logical-levels-of-nodes-in-a-document/).

```cpp
class Inline : public Aspose::Words::Node,
               public Aspose::Words::IInline,
               public Aspose::Words::Revisions::ITrackableNode
```

## Методы

| Метод | Описание |
| --- | --- |
| virtual [Accept](../node/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Принимает посетителя. |
| [Clone](../node/clone/)(bool) | Создаёт дубликат узла. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Указывает пользовательский идентификатор узла. |
| virtual [get_Document](../node/get_document/)() const | Возвращает документ, к которому принадлежит этот узел. |
| [get_Font](./get_font/)() | Предоставляет доступ к форматированию шрифта этого объекта. |
| virtual [get_IsComposite](../node/get_iscomposite/)() | Возвращает **true**, если этот узел может содержать другие узлы. |
| [get_IsDeleteRevision](./get_isdeleterevision/)() | Возвращает true, если этот объект был удалён в Microsoft Word при включённом отслеживании изменений. |
| [get_IsFormatRevision](./get_isformatrevision/)() | Возвращает true, если форматирование объекта было изменено в Microsoft Word при включённом отслеживании изменений. |
| [get_IsInsertRevision](./get_isinsertrevision/)() | Возвращает true, если этот объект был вставлен в Microsoft Word при включённом отслеживании изменений. |
| [get_IsMoveFromRevision](./get_ismovefromrevision/)() | Возвращает **true**, если этот объект был перемещён (удалён) в Microsoft Word при включённом отслеживании изменений. |
| [get_IsMoveToRevision](./get_ismovetorevision/)() | Возвращает **true**, если этот объект был перемещён (вставлен) в Microsoft Word при включённом отслеживании изменений. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Возвращает узел, непосредственно следующий за этим узлом. |
| virtual [get_NodeType](../node/get_nodetype/)() const | Возвращает тип этого узла. |
| [get_ParentNode](../node/get_parentnode/)() | Возвращает непосредственного родителя этого узла. |
| [get_ParentParagraph](./get_parentparagraph/)() | Получает родительский [Paragraph](../paragraph/) этого узла. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Возвращает узел, непосредственно предшествующий этому узлу. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Возвращает объект [Range](../range/), представляющий часть документа, содержащуюся в этом узле. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Получает первого предка указанного [NodeType](../nodetype/). |
| [GetAncestorOf](../node/getancestorof/)() |  |
| virtual [GetText](../node/gettext/)() | Получает текст этого узла и всех его дочерних узлов. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Получает следующий узел согласно алгоритму обхода дерева в порядке предобхода. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | Вспомогательный метод, преобразующий значение перечисления типа узла в удобочитаемую строку. |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Получает предыдущий узел согласно алгоритму обхода дерева в порядке предобхода. |
| [Remove](../node/remove/)() | Удаляет себя из родительского узла. |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Сеттер для [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Экспортирует содержимое узла в строку в указанном формате. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |
| static [Type](./type/)() |  |
## Примечания


Класс, производный от [Inline](./), может быть дочерним элементом [Paragraph](../paragraph/).

## Примеры



Показывает, как определить тип ревизии встроенного узла.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revision runs.docx");

// Когда мы редактируем документ при включённой опции "Track Changes", доступной через Review -> Tracking,
// в Microsoft Word, внесённые нами изменения считаются ревизиями.
// При редактировании документа с использованием Aspose.Words мы можем начать отслеживание ревизий, вызвав
// вызывая метод документа "StartTrackRevisions" и прекращая отслеживание с помощью метода "StopTrackRevisions".
// Мы можем либо принять ревизии, чтобы включить их в документ
// либо отклонить их, чтобы эффективно отменить предложенное изменение.
ASSERT_EQ(6, doc->get_Revisions()->get_Count());

// Родительским узлом ревизии является run, к которой относится ревизия. Run — это узел Inline.
auto run = System::ExplicitCast<Aspose::Words::Run>(doc->get_Revisions()->idx_get(0)->get_ParentNode());

System::SharedPtr<Aspose::Words::Paragraph> firstParagraph = run->get_ParentParagraph();
System::SharedPtr<Aspose::Words::RunCollection> runs = firstParagraph->get_Runs();

ASSERT_EQ(6, runs->ToArray()->get_Length());

// Ниже представлены пять типов ревизий, которые могут пометить Inline‑узел.
// 1 -  Вставка "insert" ревизии:
// Эта ревизия происходит, когда мы вставляем текст при отслеживании изменений.
ASSERT_TRUE(runs->idx_get(2)->get_IsInsertRevision());

// 2 -  Формат "format" ревизии:
// Эта ревизия происходит, когда мы изменяем форматирование текста при отслеживании изменений.
ASSERT_TRUE(runs->idx_get(2)->get_IsFormatRevision());

// 3 -  Ревизия "move from" ревизии:
// Когда мы выделяем текст в Microsoft Word и затем перетаскиваем его в другое место в документе
// при отслеживании изменений появляются две ревизии.
// Ревизия "move from" является копией исходного текста до его перемещения.
ASSERT_TRUE(runs->idx_get(4)->get_IsMoveFromRevision());

// 4 -  Ревизия "move to" ревизии:
// Ревизия "move to" — это текст, который мы переместили в новое положение в документе.
// Ревизии "Move from" и "move to" появляются парами для каждой выполненной нами ревизии перемещения.
// Принятие ревизии перемещения удаляет ревизию "move from" и её текст,
// и сохраняет текст из ревизии "move to".
// Отклонение ревизии перемещения, наоборот, сохраняет ревизию "move from" и удаляет ревизию "move to".
ASSERT_TRUE(runs->idx_get(1)->get_IsMoveToRevision());

// 5 -  Ревизия "delete" ревизии:
// Эта ревизия происходит, когда мы удаляем текст при отслеживании изменений. Когда мы удаляем текст таким образом,
// он останется в документе как ревизия, пока мы не примем её,
// что навсегда удалит текст, или отклонит ревизию, что сохранит удалённый текст на месте.
ASSERT_TRUE(runs->idx_get(5)->get_IsDeleteRevision());
```

## См. также

* Class [Node](../node/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
