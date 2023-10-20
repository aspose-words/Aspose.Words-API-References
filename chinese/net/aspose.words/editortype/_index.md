---
title: EditorType Enum
linktitle: EditorType
articleTitle: EditorType
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.EditorType 枚举. 指定一组可能的别名或编辑组可用作别名 to 确定是否应允许当前用户编辑由文档内可编辑范围定义的单个范围  在 C#.
type: docs
weight: 1450
url: /zh/net/aspose.words/editortype/
---
## EditorType enumeration

指定一组可能的别名（或编辑组），可用作别名 to 确定是否应允许当前用户编辑由文档内可编辑范围定义的单个范围 。

```csharp
public enum EditorType
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Unspecified | `0` | 表示没有指定编辑器类型。 |
| Administrators | `1` | 指定当启用文档保护时，应允许与管理员组关联的用户使用 此编辑类型编辑可编辑范围。 |
| Contributors | `2` | 指定当启用文档保护时，应允许与贡献者组关联的用户使用 此编辑类型编辑可编辑范围。 |
| Current | `3` | 指定当启用文档保护时，应允许与当前组关联的用户使用 this 编辑类型编辑可编辑范围。 |
| Editors | `4` | 指定当启用文档保护时，应允许与 Editors 组关联的用户使用 this 编辑类型编辑可编辑范围。 |
| Everyone | `5` | 指定在启用文档保护时，应允许所有打开文档的用户使用此 editor 类型编辑可编辑范围。 |
| None | `6` | 指定在启用文档保护时，不允许任何打开文档的用户使用此编辑类型编辑可编辑范围 。 |
| Owners | `7` | 指定当启用文档保护时，应允许与 Owners 组关联的用户使用 this 编辑类型编辑可编辑范围。 |
| Default | `0` | 同Unspecified. |

## 例子

显示如何将可编辑范围的编辑权限限制为特定组/用户。

```csharp
public void Visitor()
{
    Document doc = new Document();
    doc.Protect(ProtectionType.ReadOnly, "MyPassword");

    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.Writeln("Hello world! Since we have set the document's protection level to read-only," +
                    " we cannot edit this paragraph without the password.");

    // 当我们对文档进行写保护时，可编辑范围允许我们选择用户可以编辑的特定区域。
    // 有两种相互排斥的方法可以缩小允许的编辑器列表。
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
/// 在字符串中收集访问过的可编辑范围的属性和内容。
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

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
