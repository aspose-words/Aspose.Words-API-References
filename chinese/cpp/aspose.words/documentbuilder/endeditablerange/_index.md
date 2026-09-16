---
title: "Aspose::Words::DocumentBuilder::EndEditableRange 方法"
linktitle: "EndEditableRange"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBuilder::EndEditableRange 方法。标记文档中当前的位置为可编辑范围的结束（C++）。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words/documentbuilder/endeditablerange/
---
## DocumentBuilder::EndEditableRange() method


将文档中当前位置标记为可编辑范围结束。

```cpp
System::SharedPtr<Aspose::Words::EditableRangeEnd> Aspose::Words::DocumentBuilder::EndEditableRange()
```


### ReturnValue

刚刚创建的可编辑范围结束节点。
## 备注


文档中的可编辑范围可以重叠并跨越任意范围。要创建有效的可编辑范围，您需要同时调用 [StartEditableRange](../starteditablerange/) 和 [EndEditableRange](./) 或 [EndEditableRange()](../) 方法。

文档保存时，格式错误的可编辑范围将被忽略。

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

* Class [EditableRangeEnd](../../editablerangeend/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::EndEditableRange(const System::SharedPtr\<Aspose::Words::EditableRangeStart\>\&) method


将文档中当前位置标记为可编辑范围结束。

```cpp
System::SharedPtr<Aspose::Words::EditableRangeEnd> Aspose::Words::DocumentBuilder::EndEditableRange(const System::SharedPtr<Aspose::Words::EditableRangeStart> &start)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| start | const System::SharedPtr\<Aspose::Words::EditableRangeStart\>\& | 此可编辑范围的开始。 |

### ReturnValue

刚刚创建的可编辑范围结束节点。
## 备注


在创建嵌套可编辑范围时使用此重载。

文档中的可编辑范围可以重叠并跨越任意范围。要创建有效的可编辑范围，您需要同时调用 [StartEditableRange](../starteditablerange/) 和 [EndEditableRange](./) 或 [EndEditableRange()](../) 方法。

文档保存时，格式错误的可编辑范围将被忽略。

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

* Class [EditableRangeEnd](../../editablerangeend/)
* Class [EditableRangeStart](../../editablerangestart/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
