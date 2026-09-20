---
title: "Aspose::Words::DocumentBuilder::StartEditableRange метод"
linktitle: "StartEditableRange"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::DocumentBuilder::StartEditableRange метод. Помечает текущую позицию в документе как начало редактируемого диапазона в C++."
type: docs
weight: 70000
url: /ru/cpp/aspose.words/documentbuilder/starteditablerange/
---
## DocumentBuilder::StartEditableRange method


Помечает текущую позицию в документе как начало редактируемого диапазона.

```cpp
System::SharedPtr<Aspose::Words::EditableRangeStart> Aspose::Words::DocumentBuilder::StartEditableRange()
```


### ReturnValue

Узел начала редактируемого диапазона, который только что был создан.
## Примечания


Редактируемый диапазон в документе может перекрываться и охватывать любой диапазон. Чтобы создать корректный редактируемый диапазон, необходимо вызвать как [StartEditableRange](./), так и [EndEditableRange](../endeditablerange/) или методы [EndEditableRange()](../).

Некорректно сформированный редактируемый диапазон будет игнорироваться при сохранении документа.

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


Показывает, как создать вложенные редактируемые диапазоны.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
doc->Protect(Aspose::Words::ProtectionType::ReadOnly, u"MyPassword");

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(System::String(u"Hello world! Since we have set the document's protection level to read-only, ") + u"we cannot edit this paragraph without the password.");

// Создайте два вложенных редактируемых диапазона.
System::SharedPtr<Aspose::Words::EditableRangeStart> outerEditableRangeStart = builder->StartEditableRange();
builder->Writeln(u"This paragraph inside the outer editable range and can be edited.");

System::SharedPtr<Aspose::Words::EditableRangeStart> innerEditableRangeStart = builder->StartEditableRange();
builder->Writeln(u"This paragraph inside both the outer and inner editable ranges and can be edited.");

// В настоящее время курсор вставки узлов в DocumentBuilder находится более чем в одном активном редактируемом диапазоне.
// Когда мы хотим завершить редактируемый диапазон в этой ситуации,
// нам необходимо указать, какой из диапазонов мы хотим завершить, передав его узел EditableRangeStart.
builder->EndEditableRange(innerEditableRangeStart);

builder->Writeln(u"This paragraph inside the outer editable range and can be edited.");

builder->EndEditableRange(outerEditableRangeStart);

builder->Writeln(u"This paragraph is outside any editable ranges, and cannot be edited.");

// Если участок текста имеет два перекрывающихся редактируемых диапазона с указанными группами,
// объединённая группа пользователей, исключённая обеими группами, не может редактировать его.
outerEditableRangeStart->get_EditableRange()->set_EditorGroup(Aspose::Words::EditorType::Everyone);
innerEditableRangeStart->get_EditableRange()->set_EditorGroup(Aspose::Words::EditorType::Contributors);

doc->Save(get_ArtifactsDir() + u"EditableRange.Nested.docx");
```

## См. также

* Class [EditableRangeStart](../../editablerangestart/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
