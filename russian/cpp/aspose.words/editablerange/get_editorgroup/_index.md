---
title: "метод Aspose::Words::EditableRange::get_EditorGroup"
linktitle: "get_EditorGroup"
second_title: "Справочник API Aspose.Words для C++"
description: "метод Aspose::Words::EditableRange::get_EditorGroup. Возвращает или задает псевдоним (или группу редактирования), который будет использоваться для определения, может ли текущий пользователь редактировать этот редактируемый диапазон в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words/editablerange/get_editorgroup/
---
## EditableRange::get_EditorGroup method


Возвращает или задает псевдоним (или группу редактирования), который будет использоваться для определения, может ли текущий пользователь редактировать этот редактируемый диапазон.

```cpp
Aspose::Words::EditorType Aspose::Words::EditableRange::get_EditorGroup()
```

## Примечания


Единственный пользователь и группа редакторов не могут быть заданы одновременно для конкретного редактируемого диапазона; если один параметр установлен, другой будет сброшен.

## Примеры



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

* Enum [EditorType](../../editortype/)
* Class [EditableRange](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
