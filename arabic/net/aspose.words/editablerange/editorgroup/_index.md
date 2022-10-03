---
title: EditorGroup
second_title: Aspose.Words لمراجع .NET API
description: إرجاع أو تعيين الاسم المستعار أو مجموعة التحرير التي يجب استخدامها لتحديد ما إذا كان المستخدم الحالي مسموحًا به لتحرير هذا النطاق القابل للتحرير.
type: docs
weight: 30
url: /ar/net/aspose.words/editablerange/editorgroup/
---
## EditableRange.EditorGroup property

إرجاع أو تعيين الاسم المستعار (أو مجموعة التحرير) التي يجب استخدامها لتحديد ما إذا كان المستخدم الحالي مسموحًا به لتحرير هذا النطاق القابل للتحرير.

```csharp
public EditorType EditorGroup { get; set; }
```

### ملاحظات

لا يمكن تعيين مستخدم واحد ومجموعة محرر في وقت واحد للنطاق المحدد القابل للتحرير ، إذا تم تعيين أحدهما ، فسيكون الآخر واضحًا.

### أمثلة

يوضح كيفية إنشاء نطاقات متداخلة قابلة للتحرير.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "MyPassword");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! Since we have set the document's protection level to read-only, " +
                "we cannot edit this paragraph without the password.");

// إنشاء نطاقين متداخلين قابلين للتحرير.
EditableRangeStart outerEditableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph inside the outer editable range and can be edited.");

EditableRangeStart innerEditableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph inside both the outer and inner editable ranges and can be edited.");

// حاليًا ، يوجد مؤشر إدراج عقدة منشئ المستندات في أكثر من نطاق قابل للتحرير مستمر.
// عندما نريد إنهاء نطاق قابل للتعديل في هذه الحالة ،
// نحتاج إلى تحديد النطاقات التي نرغب في إنهاؤها بتمرير عقدة EditableRangeStart.
builder.EndEditableRange(innerEditableRangeStart);

builder.Writeln("This paragraph inside the outer editable range and can be edited.");

builder.EndEditableRange(outerEditableRangeStart);

builder.Writeln("This paragraph is outside any editable ranges, and cannot be edited.");

// إذا كانت منطقة النص تشتمل على نطاقين قابلين للتعديل متداخلين مع مجموعات محددة ،
// تم منع المجموعة المدمجة من المستخدمين المستبعدة من قبل المجموعتين من تحريرها.
outerEditableRangeStart.EditableRange.EditorGroup = EditorType.Everyone;
innerEditableRangeStart.EditableRange.EditorGroup = EditorType.Contributors;

doc.Save(ArtifactsDir + "EditableRange.Nested.docx");
```

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

* enum [EditorType](../../editortype/)
* class [EditableRange](../)
* مساحة الاسم [Aspose.Words](../../editablerange/)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
