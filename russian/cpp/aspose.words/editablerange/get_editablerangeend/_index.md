---
title: "метод Aspose::Words::EditableRange::get_EditableRangeEnd"
linktitle: "get_EditableRangeEnd"
second_title: "Справочник API Aspose.Words для C++"
description: "метод Aspose::Words::EditableRange::get_EditableRangeEnd. Получает узел, представляющий конец редактируемого диапазона в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words/editablerange/get_editablerangeend/
---
## EditableRange::get_EditableRangeEnd method


Получает узел, представляющий конец редактируемого диапазона.

```cpp
System::SharedPtr<Aspose::Words::EditableRangeEnd> Aspose::Words::EditableRange::get_EditableRangeEnd()
```


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

* Class [EditableRangeEnd](../../editablerangeend/)
* Class [EditableRange](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
