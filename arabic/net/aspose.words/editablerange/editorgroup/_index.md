---
title: EditableRange.EditorGroup
linktitle: EditorGroup
articleTitle: EditorGroup
second_title: Aspose.Words لـ .NET
description: قم بإدارة أذونات المستخدم بسهولة باستخدام خاصية EditableRange EditorGroup، مما يتيح لك التحكم في الوصول إلى التحرير لتعزيز التعاون.
type: docs
weight: 30
url: /ar/net/aspose.words/editablerange/editorgroup/
---
## EditableRange.EditorGroup property

يعيد أو يعين اسمًا مستعارًا (أو مجموعة تحرير) سيتم استخدامه لتحديد ما إذا كان المستخدم الحالي مسموحًا له بتحرير هذا النطاق القابل للتحرير.

```csharp
public EditorType EditorGroup { get; set; }
```

## ملاحظات

لا يمكن تعيين مستخدم واحد ومجموعة محرر في نفس الوقت لنطاق قابل للتحرير محدد، إذا تم تعيين أحدهما، فسيتم مسح الآخر.

## أمثلة

يوضح كيفية إنشاء نطاقات قابلة للتحرير متداخلة.

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

// حاليًا، يتواجد مؤشر إدراج عقدة منشئ المستندات في أكثر من نطاق قابل للتحرير مستمر.
// عندما نريد إنهاء نطاق قابل للتحرير في هذه الحالة،
// نحتاج إلى تحديد النطاق الذي نرغب في إنهائه عن طريق تمرير عقدة EditableRangeStart الخاصة به.
builder.EndEditableRange(innerEditableRangeStart);

builder.Writeln("This paragraph inside the outer editable range and can be edited.");

builder.EndEditableRange(outerEditableRangeStart);

builder.Writeln("This paragraph is outside any editable ranges, and cannot be edited.");

// إذا كانت منطقة النص تحتوي على نطاقين قابلين للتحرير متداخلين مع مجموعات محددة،
// يتم منع المجموعة المجمعة من المستخدمين المستبعدين من قبل كلتا المجموعتين من تحريرها.
outerEditableRangeStart.EditableRange.EditorGroup = EditorType.Everyone;
innerEditableRangeStart.EditableRange.EditorGroup = EditorType.Contributors;

doc.Save(ArtifactsDir + "EditableRange.Nested.docx");
```

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

* enum [EditorType](../../editortype/)
* class [EditableRange](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
