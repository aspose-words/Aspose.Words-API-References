---
title: "Aspose::Words::EditableRange::get_EditorGroup 方法"
linktitle: "get_EditorGroup"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::EditableRange::get_EditorGroup 方法。返回或设置别名（或编辑组），该别名用于确定当前用户是否被允许编辑此可编辑范围（在 C++ 中）。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words/editablerange/get_editorgroup/
---
## EditableRange::get_EditorGroup method


返回或设置别名（或编辑组），用于确定当前用户是否被允许编辑此可编辑范围。

```cpp
Aspose::Words::EditorType Aspose::Words::EditableRange::get_EditorGroup()
```

## 备注


对于特定的可编辑范围，单个用户和编辑器组不能同时设置；如果设置了其中一个，另一个将被清除。

## 示例



展示如何创建嵌套的可编辑范围。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
doc->Protect(Aspose::Words::ProtectionType::ReadOnly, u"MyPassword");

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(System::String(u"Hello world! Since we have set the document's protection level to read-only, ") + u"we cannot edit this paragraph without the password.");

// 创建两个嵌套的可编辑范围。
System::SharedPtr<Aspose::Words::EditableRangeStart> outerEditableRangeStart = builder->StartEditableRange();
builder->Writeln(u"This paragraph inside the outer editable range and can be edited.");

System::SharedPtr<Aspose::Words::EditableRangeStart> innerEditableRangeStart = builder->StartEditableRange();
builder->Writeln(u"This paragraph inside both the outer and inner editable ranges and can be edited.");

// 当前，文档生成器的节点插入光标位于多个正在进行的可编辑范围中。
// 当我们想在这种情况下结束一个可编辑范围时，
// 我们需要通过传递其 EditableRangeStart 节点来指定要结束的范围。
builder->EndEditableRange(innerEditableRangeStart);

builder->Writeln(u"This paragraph inside the outer editable range and can be edited.");

builder->EndEditableRange(outerEditableRangeStart);

builder->Writeln(u"This paragraph is outside any editable ranges, and cannot be edited.");

// 如果一段文本具有两个具有指定组的重叠可编辑范围，
// 被两个组共同排除的用户组合将被阻止编辑该文本。
outerEditableRangeStart->get_EditableRange()->set_EditorGroup(Aspose::Words::EditorType::Everyone);
innerEditableRangeStart->get_EditableRange()->set_EditorGroup(Aspose::Words::EditorType::Contributors);

doc->Save(get_ArtifactsDir() + u"EditableRange.Nested.docx");
```

## 另见

* Enum [EditorType](../../editortype/)
* Class [EditableRange](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
