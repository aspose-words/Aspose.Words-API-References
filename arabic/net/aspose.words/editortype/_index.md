---
title: EditorType Enum
linktitle: EditorType
articleTitle: EditorType
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.EditorType enum، الذي يُعرّف مجموعات التحرير للتحكم في أذونات المستخدم لتحرير نطاقات المستندات. حسّن إدارة مستنداتك اليوم!
type: docs
weight: 1860
url: /ar/net/aspose.words/editortype/
---
## EditorType enumeration

يحدد مجموعة الأسماء المستعارة المحتملة (أو مجموعات التحرير) التي يمكن استخدامها كأسماء مستعارة لتحديد ما إذا كان يُسمح للمستخدم الحالي بتحرير نطاق واحد محدد بواسطة نطاق قابل للتحرير ضمن مستند.

```csharp
public enum EditorType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Unspecified | `0` | يعني أن نوع المحرر غير محدد. |
| Administrators | `1` | يحدد أنه سيتم السماح للمستخدمين المرتبطين بمجموعة المسؤولين بتحرير النطاقات القابلة للتحرير باستخدام نوع التحرير هذا عندما يتم تمكين حماية المستندات. |
| Contributors | `2` | يحدد أنه سيتم السماح للمستخدمين المرتبطين بمجموعة المساهمين بتحرير النطاقات القابلة للتحرير باستخدام نوع التحرير هذا عندما يتم تمكين حماية المستندات. |
| Current | `3` | يحدد أنه سيتم السماح للمستخدمين المرتبطين بالمجموعة الحالية بتحرير النطاقات القابلة للتحرير باستخدام نوع التحرير this عندما يتم تمكين حماية المستند. |
| Editors | `4` | يحدد أنه سيتم السماح للمستخدمين المرتبطين بمجموعة المحررين بتحرير النطاقات القابلة للتحرير باستخدام نوع التحرير this عندما يتم تمكين حماية المستند. |
| Everyone | `5` | يحدد أنه سيتم السماح لجميع المستخدمين الذين يفتحون المستند بتحرير النطاقات القابلة للتحرير باستخدام نوع editing هذا عندما يتم تمكين حماية المستند. |
| None | `6` | يحدد أنه لن يُسمح لأي من المستخدمين الذين يفتحون المستند بتحرير النطاقات القابلة للتحرير باستخدام نوع التحرير هذا عندما يتم تمكين حماية المستند. |
| Owners | `7` | يحدد أنه سيتم السماح للمستخدمين المرتبطين بمجموعة المالكين بتحرير النطاقات القابلة للتحرير باستخدام نوع التحرير this عندما يتم تمكين حماية المستند. |
| Default | `0` | نفس الشيءUnspecified . |

## أمثلة

يوضح كيفية تقييد حقوق تحرير النطاقات القابلة للتحرير لمجموعة/مستخدم محدد.

```csharp
public void Visitor()
{
    Document doc = new Document();
    doc.Protect(ProtectionType.ReadOnly, "MyPassword");

    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.Writeln("Hello world! Since we have set the document's protection level to read-only," +
                    " we cannot edit this paragraph without the password.");

    // عندما نقوم بحماية المستندات ضد الكتابة، فإن النطاقات القابلة للتحرير تسمح لنا باختيار مناطق معينة يمكن للمستخدمين تحريرها.
    // هناك طريقتان متبادلتان لتضييق قائمة المحررين المسموح لهم.
    // 1 - تحديد المستخدم:
    EditableRange editableRange = builder.StartEditableRange().EditableRange;
    editableRange.SingleUser = "john.doe@myoffice.com";
    builder.Writeln($"This paragraph is inside the first editable range, can only be edited by {editableRange.SingleUser}.");
    builder.EndEditableRange();

    Assert.AreEqual(EditorType.Unspecified, editableRange.EditorGroup);

    // 2 - حدد المجموعة التي يسمح للمستخدمين بالارتباط بها:
    editableRange = builder.StartEditableRange().EditableRange;
    editableRange.EditorGroup = EditorType.Administrators;
    builder.Writeln($"This paragraph is inside the first editable range, can only be edited by {editableRange.EditorGroup}.");
    builder.EndEditableRange();

    Assert.AreEqual(string.Empty, editableRange.SingleUser);

    builder.Writeln("This paragraph is outside the editable range, and cannot be edited by anybody.");

    // طباعة تفاصيل ومحتويات كل نطاق قابل للتحرير في المستند.
    EditableRangePrinter editableRangePrinter = new EditableRangePrinter();

    doc.Accept(editableRangePrinter);

    Console.WriteLine(editableRangePrinter.ToText());
}

/// <summary>
/// يجمع خصائص ومحتويات النطاقات القابلة للتحرير التي تمت زيارتها في سلسلة.
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
    /// يتم استدعاؤها عند مواجهة عقدة EditableRangeStart في المستند.
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
    /// يتم استدعاؤها عند مواجهة عقدة EditableRangeEnd في المستند.
    /// </summary>
    public override VisitorAction VisitEditableRangeEnd(EditableRangeEnd editableRangeEnd)
    {
        mBuilder.AppendLine(" -- End of editable range --\n");

        mInsideEditableRange = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يُستدعى عند وجود عقدة تشغيل في المستند. يُسجل هذا الزائر فقط عمليات التشغيل التي تقع ضمن نطاقات قابلة للتعديل.
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

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
