---
title: EditableRange Class
linktitle: EditableRange
articleTitle: EditableRange
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.EditableRange 班级. 表示单个可编辑范围 在 C#.
type: docs
weight: 1420
url: /zh/net/aspose.words/editablerange/
---
## EditableRange class

表示单个可编辑范围。

要了解更多信息，请访问[Aspose.Words 文档对象模型 (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/)文档文章。

```csharp
public class EditableRange
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [EditableRangeEnd](../../aspose.words/editablerange/editablerangeend/) { get; } | 获取表示可编辑范围末尾的节点。 |
| [EditableRangeStart](../../aspose.words/editablerange/editablerangestart/) { get; } | 获取表示可编辑范围开始的节点。 |
| [EditorGroup](../../aspose.words/editablerange/editorgroup/) { get; set; } | 返回或设置别名（或编辑组），用于确定是否允许当前用户 编辑此可编辑范围。 |
| [Id](../../aspose.words/editablerange/id/) { get; } | 获取可编辑范围标识符。 |
| [SingleUser](../../aspose.words/editablerange/singleuser/) { get; set; } | 返回或设置可编辑范围的单个用户。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Remove](../../aspose.words/editablerange/remove/)() | 从文档中删除可编辑范围。不删除可编辑范围内的内容。 |

## 评论

`EditableRange`是一个封装了两个节点的“facade”对象[`EditableRangeStart`](./editablerangestart/) 和[`EditableRangeEnd`](./editablerangeend/)在文档树中，并允许将可编辑范围作为单个对象使用。

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

展示如何将可编辑范围的编辑权限限制为特定组/用户。

```csharp
public void Visitor()
{
    Document doc = new Document();
    doc.Protect(ProtectionType.ReadOnly, "MyPassword");

    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.Writeln("Hello world! Since we have set the document's protection level to read-only," +
                    " we cannot edit this paragraph without the password.");

    // 当我们对文档进行写保护时，可编辑范围允许我们选择用户可以编辑的特定区域。
    // 有两种互斥的方法来缩小允许的编辑器列表的范围。
    // 1 - 指定用户：
    EditableRange editableRange = builder.StartEditableRange().EditableRange;
    editableRange.SingleUser = "john.doe@myoffice.com";
    builder.Writeln($"This paragraph is inside the first editable range, can only be edited by {editableRange.SingleUser}.");
    builder.EndEditableRange();

    Assert.AreEqual(EditorType.Unspecified, editableRange.EditorGroup);

    // 2 - 指定允许用户关联的组：
    editableRange = builder.StartEditableRange().EditableRange;
    editableRange.EditorGroup = EditorType.Administrators;
    builder.Writeln($"This paragraph is inside the first editable range, can only be edited by {editableRange.EditorGroup}.");
    builder.EndEditableRange();

    Assert.AreEqual(string.Empty, editableRange.SingleUser);

    builder.Writeln("This paragraph is outside the editable range, and cannot be edited by anybody.");

    // 打印文档中每个可编辑范围的详细信息和内容。
    EditableRangePrinter editableRangePrinter = new EditableRangePrinter();

    doc.Accept(editableRangePrinter);

    Console.WriteLine(editableRangePrinter.ToText());
}

/// <summary>
/// 收集字符串中访问过的可编辑范围的属性和内容。
/// </summary>
public class EditableRangePrinter : DocumentVisitor
{
    public EditableRangePrinter()
    {
        mBuilder = new StringBuilder();
    }

    public string ToText()
    {
        return mBuilder.ToString();
    }

    public void Reset()
    {
        mBuilder.Clear();
        mInsideEditableRange = false;
    }

    /// <summary>
    /// 在文档中遇到 EditableRangeStart 节点时调用。
    /// </summary>
    public override VisitorAction VisitEditableRangeStart(EditableRangeStart editableRangeStart)
    {
        mBuilder.AppendLine(" -- Editable range found! -- ");
        mBuilder.AppendLine("\tID:\t\t" + editableRangeStart.Id);
        if (editableRangeStart.EditableRange.SingleUser == string.Empty)
            mBuilder.AppendLine("\tGroup:\t" + editableRangeStart.EditableRange.EditorGroup);
        else
            mBuilder.AppendLine("\tUser:\t" + editableRangeStart.EditableRange.SingleUser);
        mBuilder.AppendLine("\tContents:");

        mInsideEditableRange = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 在文档中遇到 EditableRangeEnd 节点时调用。
    /// </summary>
    public override VisitorAction VisitEditableRangeEnd(EditableRangeEnd editableRangeEnd)
    {
        mBuilder.AppendLine(" -- End of editable range --\n");

        mInsideEditableRange = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 在文档中遇到 Run 节点时调用。该访问者仅记录可编辑范围内的运行。
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mInsideEditableRange) mBuilder.AppendLine("\t\"" + run.Text + "\"");

        return VisitorAction.Continue;
    }

    private bool mInsideEditableRange;
    private readonly StringBuilder mBuilder;
}
```

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
