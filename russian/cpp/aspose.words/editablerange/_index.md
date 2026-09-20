---
title: "Класс Aspose::Words::EditableRange"
linktitle: "EditableRange"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::EditableRange class. Представляет один редактируемый диапазон. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 24000
url: /ru/cpp/aspose.words/editablerange/
---
## EditableRange class


Представляет один редактируемый диапазон. Чтобы узнать больше, посетите статью документации [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class EditableRange : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_EditableRangeEnd](./get_editablerangeend/)() | Получает узел, представляющий конец редактируемого диапазона. |
| [get_EditableRangeStart](./get_editablerangestart/)() const | Получает узел, представляющий начало редактируемого диапазона. |
| [get_EditorGroup](./get_editorgroup/)() | Возвращает или задает псевдоним (или группу редактирования), который будет использоваться для определения, может ли текущий пользователь редактировать этот редактируемый диапазон. |
| [get_Id](./get_id/)() | Получает идентификатор редактируемого диапазона. |
| [get_SingleUser](./get_singleuser/)() | Возвращает или задает единственного пользователя для редактируемого диапазона. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Удаляет редактируемый диапазон из документа. Не удаляет содержимое внутри редактируемого диапазона. |
| [set_EditorGroup](./set_editorgroup/)(Aspose::Words::EditorType) | Сеттер для [Aspose::Words::EditableRange::get_EditorGroup](./get_editorgroup/). |
| [set_SingleUser](./set_singleuser/)(const System::String\&) | Сеттер для [Aspose::Words::EditableRange::get_SingleUser](./get_singleuser/). |
| static [Type](./type/)() |  |
## Примечания


[EditableRange](./) is a "facade" object that encapsulates two nodes [EditableRangeStart](./get_editablerangestart/) and [EditableRangeEnd](./get_editablerangeend/) in a document tree and allows to work with an editable range as a single object.

## Примеры



Показывает, как работать с редактируемым диапазоном.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
doc->Protect(Aspose::Words::ProtectionType::ReadOnly, u"MyPassword");

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(System::String(u"Hello world! Since we have set the document's protection level to read-only,") + u" we cannot edit this paragraph without the password.");

// Редактируемые диапазоны позволяют оставлять части защищённых документов открытыми для редактирования.
System::SharedPtr<Aspose::Words::EditableRangeStart> editableRangeStart = builder->StartEditableRange();
builder->Writeln(u"This paragraph is inside an editable range, and can be edited.");
System::SharedPtr<Aspose::Words::EditableRangeEnd> editableRangeEnd = builder->EndEditableRange();

// Корректно сформированный редактируемый диапазон имеет начальный и конечный узлы.
// Эти узлы имеют совпадающие идентификаторы и охватывают редактируемые узлы.
System::SharedPtr<Aspose::Words::EditableRange> editableRange = editableRangeStart->get_EditableRange();

ASSERT_EQ(editableRangeStart->get_Id(), editableRange->get_Id());
ASSERT_EQ(editableRangeEnd->get_Id(), editableRange->get_Id());

// Разные части редактируемого диапазона связаны друг с другом.
ASSERT_EQ(editableRangeStart->get_Id(), editableRange->get_EditableRangeStart()->get_Id());
ASSERT_EQ(editableRangeStart->get_Id(), editableRangeEnd->get_EditableRangeStart()->get_Id());
ASSERT_EQ(editableRange->get_Id(), editableRangeStart->get_EditableRange()->get_Id());
ASSERT_EQ(editableRangeEnd->get_Id(), editableRange->get_EditableRangeEnd()->get_Id());

// Мы можем получить типы узлов каждой части так. Сам редактируемый диапазон не является узлом,
// а является сущностью, состоящей из начала, конца и их вложенного содержимого.
ASSERT_EQ(Aspose::Words::NodeType::EditableRangeStart, editableRangeStart->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::EditableRangeEnd, editableRangeEnd->get_NodeType());

builder->Writeln(u"This paragraph is outside the editable range, and cannot be edited.");

doc->Save(get_ArtifactsDir() + u"EditableRange.CreateAndRemove.docx");

// Удалите редактируемый диапазон. Все узлы, находившиеся внутри диапазона, останутся нетронутыми.
editableRange->Remove();
```

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
