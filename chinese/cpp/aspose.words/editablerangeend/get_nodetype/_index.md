---
title: "Aspose::Words::EditableRangeEnd::get_NodeType 方法"
linktitle: "get_NodeType"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::EditableRangeEnd::get_NodeType 方法。C++ 中返回 EditableRangeEnd。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words/editablerangeend/get_nodetype/
---
## EditableRangeEnd::get_NodeType method


返回 [EditableRangeEnd](../../nodetype/)。

```cpp
Aspose::Words::NodeType Aspose::Words::EditableRangeEnd::get_NodeType() const override
```


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

* Enum [NodeType](../../nodetype/)
* Class [EditableRangeEnd](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
