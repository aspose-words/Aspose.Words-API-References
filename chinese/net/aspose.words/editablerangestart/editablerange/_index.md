---
title: EditableRangeStart.EditableRange
linktitle: EditableRange
articleTitle: EditableRange
second_title: Aspose.Words for .NET
description: 探索 EditableRangeStart 属性，轻松管理可编辑范围的关键。轻松访问和控制您的内容！
type: docs
weight: 10
url: /zh/net/aspose.words/editablerangestart/editablerange/
---
## EditableRangeStart.EditableRange property

获取封装此可编辑范围开始和结束的外观对象。

```csharp
public EditableRange EditableRange { get; }
```

## 例子

展示如何使用可编辑范围。

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "MyPassword");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! Since we have set the document's protection level to read-only," +
                " we cannot edit this paragraph without the password.");

// 可编辑范围允许我们将受保护文档的部分内容保持开放以供编辑。
EditableRangeStart editableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph is inside an editable range, and can be edited.");
EditableRangeEnd editableRangeEnd = builder.EndEditableRange();

// 格式良好的可编辑范围有一个起始节点和结束节点。
// 这些节点具有匹配的 ID 并包含可编辑节点。
EditableRange editableRange = editableRangeStart.EditableRange;

Assert.AreEqual(editableRangeStart.Id, editableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.Id);

// 可编辑范围的不同部分相互链接。
Assert.AreEqual(editableRangeStart.Id, editableRange.EditableRangeStart.Id);
Assert.AreEqual(editableRangeStart.Id, editableRangeEnd.EditableRangeStart.Id);
Assert.AreEqual(editableRange.Id, editableRangeStart.EditableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.EditableRangeEnd.Id);

// 我们可以像这样访问每个部分的节点类型。可编辑范围本身不是节点，
// 而是一个由开始、结束及其所包含的内容组成的实体。
Assert.AreEqual(NodeType.EditableRangeStart, editableRangeStart.NodeType);
Assert.AreEqual(NodeType.EditableRangeEnd, editableRangeEnd.NodeType);

builder.Writeln("This paragraph is outside the editable range, and cannot be edited.");

doc.Save(ArtifactsDir + "EditableRange.CreateAndRemove.docx");

// 删除可编辑范围。范围内的所有节点将保持不变。
editableRange.Remove();
```

### 也可以看看

* class [EditableRange](../../editablerange/)
* class [EditableRangeStart](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
