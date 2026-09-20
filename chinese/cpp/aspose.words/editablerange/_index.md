---
title: "Aspose::Words::EditableRange 类"
linktitle: "EditableRange"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::EditableRange 类。表示单个可编辑范围。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 24000
url: /zh/cpp/aspose.words/editablerange/
---
## EditableRange class


表示单个可编辑范围。要了解更多信息，请访问 [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/) 文档文章。

```cpp
class EditableRange : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_EditableRangeEnd](./get_editablerangeend/)() | 获取表示可编辑范围结束的节点。 |
| [get_EditableRangeStart](./get_editablerangestart/)() const | 获取表示可编辑范围开始的节点。 |
| [get_EditorGroup](./get_editorgroup/)() | 返回或设置别名（或编辑组），用于确定当前用户是否被允许编辑此可编辑范围。 |
| [get_Id](./get_id/)() | 获取可编辑范围标识符。 |
| [get_SingleUser](./get_singleuser/)() | 返回或设置可编辑范围的单一用户。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | 从文档中移除可编辑范围。但不会删除可编辑范围内的内容。 |
| [set_EditorGroup](./set_editorgroup/)(Aspose::Words::EditorType) | 用于 [Aspose::Words::EditableRange::get_EditorGroup](./get_editorgroup/) 的设置器。 |
| [set_SingleUser](./set_singleuser/)(const System::String\&) | 用于 [Aspose::Words::EditableRange::get_SingleUser](./get_singleuser/) 的设置器。 |
| static [Type](./type/)() |  |
## 备注


[EditableRange](./) is a "facade" object that encapsulates two nodes [EditableRangeStart](./get_editablerangestart/) and [EditableRangeEnd](./get_editablerangeend/) in a document tree and allows to work with an editable range as a single object.

## 示例



展示如何使用可编辑范围。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
doc->Protect(Aspose::Words::ProtectionType::ReadOnly, u"MyPassword");

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(System::String(u"Hello world! Since we have set the document's protection level to read-only,") + u" we cannot edit this paragraph without the password.");

// 可编辑范围允许我们在受保护的文档中保留可编辑的部分。
System::SharedPtr<Aspose::Words::EditableRangeStart> editableRangeStart = builder->StartEditableRange();
builder->Writeln(u"This paragraph is inside an editable range, and can be edited.");
System::SharedPtr<Aspose::Words::EditableRangeEnd> editableRangeEnd = builder->EndEditableRange();

// 一个结构良好的可编辑范围具有起始节点和结束节点。
// 这些节点具有匹配的 ID，并包含可编辑节点。
System::SharedPtr<Aspose::Words::EditableRange> editableRange = editableRangeStart->get_EditableRange();

ASSERT_EQ(editableRangeStart->get_Id(), editableRange->get_Id());
ASSERT_EQ(editableRangeEnd->get_Id(), editableRange->get_Id());

// 可编辑范围的不同部分相互链接。
ASSERT_EQ(editableRangeStart->get_Id(), editableRange->get_EditableRangeStart()->get_Id());
ASSERT_EQ(editableRangeStart->get_Id(), editableRangeEnd->get_EditableRangeStart()->get_Id());
ASSERT_EQ(editableRange->get_Id(), editableRangeStart->get_EditableRange()->get_Id());
ASSERT_EQ(editableRangeEnd->get_Id(), editableRange->get_EditableRangeEnd()->get_Id());

// 我们可以这样访问每个部分的节点类型。可编辑范围本身不是节点，
// 而是一个由起始、结束及其包含内容组成的实体。
ASSERT_EQ(Aspose::Words::NodeType::EditableRangeStart, editableRangeStart->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::EditableRangeEnd, editableRangeEnd->get_NodeType());

builder->Writeln(u"This paragraph is outside the editable range, and cannot be edited.");

doc->Save(get_ArtifactsDir() + u"EditableRange.CreateAndRemove.docx");

// 删除可编辑范围。范围内的所有节点将保持完整。
editableRange->Remove();
```

## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
