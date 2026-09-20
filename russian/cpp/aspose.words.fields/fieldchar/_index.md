---
title: "Aspose::Words::Fields::FieldChar класс"
linktitle: "FieldChar"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldChar класс. Базовый класс для узлов, представляющих символы полей в документе. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 21000
url: /ru/cpp/aspose.words.fields/fieldchar/
---
## FieldChar class


Базовый класс для узлов, представляющих символы поля в документе. Чтобы узнать больше, посетите статью документации [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldChar : public Aspose::Words::SpecialChar
```

## Методы

| Метод | Описание |
| --- | --- |
| [Accept](../../aspose.words/specialchar/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Принимает посетителя. |
| [Clone](../../aspose.words/node/clone/)(bool) | Создаёт дубликат узла. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Указывает пользовательский идентификатор узла. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Возвращает документ, к которому принадлежит этот узел. |
| [get_FieldType](./get_fieldtype/)() const | Возвращает тип поля. |
| [get_Font](../../aspose.words/inline/get_font/)() | Предоставляет доступ к форматированию шрифта этого объекта. |
| virtual [get_IsComposite](../../aspose.words/node/get_iscomposite/)() | Возвращает **true**, если этот узел может содержать другие узлы. |
| [get_IsDeleteRevision](../../aspose.words/inline/get_isdeleterevision/)() | Возвращает true, если этот объект был удалён в Microsoft Word при включённом отслеживании изменений. |
| [get_IsDirty](./get_isdirty/)() const | Получает или задает, является ли текущий результат поля более некорректным (устаревшим) из‑за других изменений, внесённых в документ. |
| [get_IsFormatRevision](../../aspose.words/inline/get_isformatrevision/)() | Возвращает true, если форматирование объекта было изменено в Microsoft Word при включённом отслеживании изменений. |
| [get_IsInsertRevision](../../aspose.words/inline/get_isinsertrevision/)() | Возвращает true, если этот объект был вставлен в Microsoft Word при включённом отслеживании изменений. |
| [get_IsLocked](./get_islocked/)() const | Получает или задает, заблокировано ли родительское поле (не должно пересчитывать свой результат). |
| [get_IsMoveFromRevision](../../aspose.words/inline/get_ismovefromrevision/)() | Возвращает **true**, если этот объект был перемещён (удалён) в Microsoft Word при включённом отслеживании изменений. |
| [get_IsMoveToRevision](../../aspose.words/inline/get_ismovetorevision/)() | Возвращает **true**, если этот объект был перемещён (вставлен) в Microsoft Word при включённом отслеживании изменений. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Возвращает узел, непосредственно следующий за этим узлом. |
| [get_NodeType](../../aspose.words/specialchar/get_nodetype/)() const override | Возвращает [SpecialChar](../../aspose.words/nodetype/). |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Возвращает непосредственного родителя этого узла. |
| [get_ParentParagraph](../../aspose.words/inline/get_parentparagraph/)() | Получает родительский [Paragraph](../../aspose.words/paragraph/) этого узла. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Возвращает узел, непосредственно предшествующий этому узлу. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Возвращает объект [Range](../../aspose.words/range/), представляющий часть документа, содержащуюся в этом узле. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Возвращает первого предка указанного [NodeType](../../aspose.words/nodetype/). |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetField](./getfield/)() | Возвращает поле для символа поля. |
| [GetText](../../aspose.words/specialchar/gettext/)() override | Получает специальный символ, который представляет этот узел. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Получает следующий узел согласно алгоритму обхода дерева в порядке предобхода. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | Вспомогательный метод, преобразующий значение перечисления типа узла в удобочитаемую строку. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Получает предыдущий узел согласно алгоритму обхода дерева в порядке предобхода. |
| [Remove](../../aspose.words/node/remove/)() | Удаляет себя из родительского узла. |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Сеттер для [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_IsDirty](./set_isdirty/)(bool) | Сеттер для [Aspose::Words::Fields::FieldChar::get_IsDirty](./get_isdirty/). |
| [set_IsLocked](./set_islocked/)(bool) | Сеттер для [Aspose::Words::Fields::FieldChar::get_IsLocked](./get_islocked/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Экспортирует содержимое узла в строку в указанном формате. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |
| static [Type](./type/)() |  |
## Примечания


Полное поле в документе Microsoft Word представляет собой сложную структуру, состоящую из символа начала поля, кода поля, символа-разделителя, результата поля и символа конца поля. Некоторые поля содержат только начало поля, код поля и конец поля.

Чтобы легко вставить новое поле в документ, используйте метод [InsertField()](../).

## Примеры



Показывает, как работать с узлом [FieldStart](../fieldstart/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->get_Format()->set_DateTimeFormat(u"dddd, MMMM dd, yyyy");
field->Update();

System::SharedPtr<Aspose::Words::Fields::FieldChar> fieldStart = field->get_Start();

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, fieldStart->get_FieldType());
ASPOSE_ASSERT_EQ(false, fieldStart->get_IsDirty());
ASPOSE_ASSERT_EQ(false, fieldStart->get_IsLocked());

// Получите объект фасада, представляющий поле в документе.
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(fieldStart->GetField());

ASPOSE_ASSERT_EQ(false, field->get_IsLocked());
ASSERT_EQ(u" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// Обновите поле, чтобы отобразить текущую дату.
field->Update();
```

## См. также

* Class [SpecialChar](../../aspose.words/specialchar/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
