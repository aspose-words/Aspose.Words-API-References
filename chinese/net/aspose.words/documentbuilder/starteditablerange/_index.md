---
title: StartEditableRange
second_title: Aspose.Words for .NET API 参考
description: 将文档中的当前位置标记为可编辑范围开始
type: docs
weight: 600
url: /zh/net/aspose.words/documentbuilder/starteditablerange/
---
## DocumentBuilder.StartEditableRange method

将文档中的当前位置标记为可编辑范围开始。

```csharp
public EditableRangeStart StartEditableRange()
```

### 返回值

刚刚创建的可编辑范围起始节点。

### 评论

文档中的可编辑范围可以重叠并跨越任何范围。要创建有效的可编辑范围，您需要 to 调用两者`StartEditableRange`和[`EndEditableRange`](../endeditablerange) 或[`EndEditableRange`](../endeditablerange)方法。

保存文档时将忽略格式错误的可编辑范围。

### 例子

展示如何创建嵌套的可编辑范围。

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "MyPassword");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! Since we have set the document's protection level to read-only, " +
                "we cannot edit this paragraph without the password.");

// 创建两个嵌套的可编辑范围。
EditableRangeStart outerEditableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph inside the outer editable range and can be edited.");

EditableRangeStart innerEditableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph inside both the outer and inner editable ranges and can be edited.");

// 目前，文档构建器的节点插入光标位于多个正在进行的可编辑范围内。
// 当我们想在这种情况下结束一个可编辑的范围时，
// 我们需要通过传递 EditableRangeStart 节点来指定我们希望结束的范围。
builder.EndEditableRange(innerEditableRangeStart);

builder.Writeln("This paragraph inside the outer editable range and can be edited.");

builder.EndEditableRange(outerEditableRangeStart);

builder.Writeln("This paragraph is outside any editable ranges, and cannot be edited.");

// 如果一个文本区域有两个重叠的可编辑范围和指定的组，
// 防止被两个组排除的用户组合组对其进行编辑。
outerEditableRangeStart.EditableRange.EditorGroup = EditorType.Everyone;
innerEditableRangeStart.EditableRange.EditorGroup = EditorType.Contributors;

doc.Save(ArtifactsDir + "EditableRange.Nested.docx");
```

展示如何使用可编辑范围。

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "MyPassword");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! Since we have set the document's protection level to read-only," +
                " we cannot edit this paragraph without the password.");

// 可编辑范围允许我们将受保护文档的部分保留打开以进行编辑。
EditableRangeStart editableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph is inside an editable range, and can be edited.");
EditableRangeEnd editableRangeEnd = builder.EndEditableRange();

// 一个格式良好的可编辑范围有一个开始节点和结束节点。
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
// 而是一个由开始、结束和它们所包含的内容组成的实体。
Assert.AreEqual(NodeType.EditableRangeStart, editableRangeStart.NodeType);
Assert.AreEqual(NodeType.EditableRangeEnd, editableRangeEnd.NodeType);

builder.Writeln("This paragraph is outside the editable range, and cannot be edited.");

doc.Save(ArtifactsDir + "EditableRange.CreateAndRemove.docx");

// 删除一个可编辑的范围。范围内的所有节点都将保持不变。
editableRange.Remove();
```

### 也可以看看

* class [EditableRangeStart](../../editablerangestart)
* class [DocumentBuilder](../../documentbuilder)
* 命名空间 [Aspose.Words](../../documentbuilder)
* 部件 [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->