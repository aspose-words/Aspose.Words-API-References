---
title: EditableRange.SingleUser
linktitle: SingleUser
articleTitle: SingleUser
second_title: Aspose.Words for .NET
description: 发现 EditableRange SingleUser 属性以有效管理可编辑范围，确保无缝协作和特定于用户的访问控制。
type: docs
weight: 50
url: /zh/net/aspose.words/editablerange/singleuser/
---
## EditableRange.SingleUser property

返回或设置可编辑范围的单个用户。

```csharp
public string SingleUser { get; set; }
```

## 评论

该编辑器可以采用以下形式之一存储：

DOMAIN\Username - 针对需要使用当前用户的域凭据来验证访问权限的用户。

user@domain.com - 适用于使用用户的电子邮件地址作为凭证来验证其访问权限的用户。

用户 - 针对需要使用当前用户的机器凭证来验证访问权限的用户。

单个用户与编辑者组不能同时设置具体的可编辑范围， 如果设置了一个，另一个将被清除。

## 例子

展示如何将可编辑范围的编辑权限限制给特定的组/用户。

```csharp
public void Visitor()
{
    Document doc = new Document();
    doc.Protect(ProtectionType.ReadOnly, "MyPassword");

    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.Writeln("Hello world! Since we have set the document's protection level to read-only," +
                    " we cannot edit this paragraph without the password.");

    // 当我们对文档进行写保护时，可编辑范围允许我们选择用户可以编辑的特定区域。
    // 有两种互斥的方法来缩小允许的编辑器列表。
    // 1 - 指定用户：
    EditableRange editableRange = builder.StartEditableRange().EditableRange;
    editableRange.SingleUser = "john.doe@myoffice.com";
    builder.Writeln($"This paragraph is inside the first editable range, can only be edited by {editableRange.SingleUser}.");
    builder.EndEditableRange();

    Assert.AreEqual(EditorType.Unspecified, editableRange.EditorGroup);

    // 2 - 指定允许的用户所关联的组：
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
/// 在字符串中收集已访问的可编辑范围的属性和内容。
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
    /// 当在文档中遇到 EditableRangeStart 节点时调用。
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
    /// 当在文档中遇到 EditableRangeEnd 节点时调用。
    /// </summary>
    public override VisitorAction VisitEditableRangeEnd(EditableRangeEnd editableRangeEnd)
    {
        mBuilder.AppendLine(" -- End of editable range --\n");

        mInsideEditableRange = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 在文档中遇到 Run 节点时调用。此访问者仅记录可编辑范围内的运行。
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

* class [EditableRange](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
