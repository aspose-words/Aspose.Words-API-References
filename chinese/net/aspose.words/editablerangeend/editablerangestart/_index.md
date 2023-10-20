---
title: EditableRangeEnd.EditableRangeStart
linktitle: EditableRangeStart
articleTitle: EditableRangeStart
second_title: 用于 .NET 的 Aspose.Words
description: EditableRangeEnd EditableRangeStart 财产. 对应EditableRangeStart由 ID. 接收 在 C#.
type: docs
weight: 10
url: /zh/net/aspose.words/editablerangeend/editablerangestart/
---
## EditableRangeEnd.EditableRangeStart property

对应[`EditableRangeStart`](../../editablerangestart/)，由 ID. 接收

```csharp
public EditableRangeStart EditableRangeStart { get; }
```

## 例子

展示如何使用可编辑范围。

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "MyPassword");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! Since we have set the document's protection level to read-only," +
                " we cannot edit this paragraph without the password.");

// 可编辑范围允许我们保留受保护文档的部分内容以供编辑。
EditableRangeStart editableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph is inside an editable range, and can be edited.");
EditableRangeEnd editableRangeEnd = builder.EndEditableRange();

// 格式良好的可编辑范围具有起始节点和结束节点。
// 这些节点具有匹配的 ID 并包含可编辑节点。
EditableRange editableRange = editableRangeStart.EditableRange;

Assert.AreEqual(editableRangeStart.Id, editableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.Id);

// 可编辑范围的不同部分相互链接。
Assert.AreEqual(editableRangeStart.Id, editableRange.EditableRangeStart.Id);
Assert.AreEqual(editableRangeStart.Id, editableRangeEnd.EditableRangeStart.Id);
Assert.AreEqual(editableRange.Id, editableRangeStart.EditableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.EditableRangeEnd.Id);

// 我们可以像这样访问每个部分的节点类型。可编辑范围本身不是一个节点，
// 而是一个由开始、结束及其包含的内容组成的实体。
Assert.AreEqual(NodeType.EditableRangeStart, editableRangeStart.NodeType);
Assert.AreEqual(NodeType.EditableRangeEnd, editableRangeEnd.NodeType);

builder.Writeln("This paragraph is outside the editable range, and cannot be edited.");

doc.Save(ArtifactsDir + "EditableRange.CreateAndRemove.docx");

// 删除可编辑范围。该范围内的所有节点将保持不变。
editableRange.Remove();
```

### 也可以看看

* class [EditableRangeStart](../../editablerangestart/)
* class [EditableRangeEnd](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
