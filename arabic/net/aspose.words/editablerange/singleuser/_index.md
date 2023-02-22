---
title: EditableRange.SingleUser
second_title: Aspose.Words لمراجع .NET API
description: EditableRange ملكية. إرجاع أو تعيين المستخدم الفردي للنطاق القابل للتحرير.
type: docs
weight: 50
url: /ar/net/aspose.words/editablerange/singleuser/
---
## EditableRange.SingleUser property

إرجاع أو تعيين المستخدم الفردي للنطاق القابل للتحرير.

```csharp
public string SingleUser { get; set; }
```

### ملاحظات

يمكن تخزين هذا المحرر بأحد الأشكال التالية:

المجال \ اسم المستخدم - للمستخدمين الذين يجب مصادقة وصولهم باستخدام بيانات اعتماد مجال المستخدم الحالي.

user@domain.com - للمستخدمين الذين يجب مصادقة وصولهم باستخدام عنوان البريد الإلكتروني للمستخدم كأوراق اعتماد.

مستخدم - للمستخدمين الذين يجب مصادقة وصولهم باستخدام بيانات اعتماد جهاز المستخدم الحالي.

لا يمكن تعيين مستخدم واحد ومجموعة محرر في وقت واحد للنطاق المحدد القابل للتحرير ، إذا تم تعيين أحدهما ، فسيكون الآخر واضحًا.

### أمثلة

يوضح كيفية تقييد حقوق التحرير للنطاقات القابلة للتحرير لمجموعة / مستخدم معين.

```csharp
public void Visitor()
{
    Document doc = new Document();
    doc.Protect(ProtectionType.ReadOnly, "MyPassword");

    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.Writeln("Hello world! Since we have set the document's protection level to read-only," +
                    " we cannot edit this paragraph without the password.");

    // عندما نكتب حماية المستندات ، تسمح لنا النطاقات القابلة للتحرير باختيار مناطق محددة يمكن للمستخدمين تحريرها.
    // هناك طريقتان متنافيتان لتضييق نطاق قائمة المحررين المسموح لهم.
    // 1 - حدد مستخدمًا:
    EditableRange editableRange = builder.StartEditableRange().EditableRange;
    editableRange.SingleUser = "john.doe@myoffice.com";
    builder.Writeln($"This paragraph is inside the first editable range, can only be edited by {editableRange.SingleUser}.");
    builder.EndEditableRange();

    Assert.AreEqual(EditorType.Unspecified, editableRange.EditorGroup);

    // 2 - حدد مجموعة يرتبط بها المستخدمون المسموح لهم بـ:
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
    /// يتم الاستدعاء عند مواجهة عقدة EditableRangeStart في المستند.
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
    /// يتم الاستدعاء عند مواجهة عقدة EditableRangeEnd في المستند.
    /// </summary>
    public override VisitorAction VisitEditableRangeEnd(EditableRangeEnd editableRangeEnd)
    {
        mBuilder.AppendLine(" -- End of editable range --\n");

        mInsideEditableRange = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم الاستدعاء عند مواجهة عقدة تشغيل في المستند. يسجل هذا الزائر فقط عمليات التشغيل الموجودة داخل نطاقات قابلة للتحرير.
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

* class [EditableRange](../)
* مساحة الاسم [Aspose.Words](../../editablerange/)
* المجسم [Aspose.Words](../../../)


