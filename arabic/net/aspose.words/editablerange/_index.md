---
title: EditableRange Class
linktitle: EditableRange
articleTitle: EditableRange
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.EditableRange، الحل الأمثل لإدارة مساحات النصوص القابلة للتعديل بسهولة. حسّن تحرير المستندات بسهولة!
type: docs
weight: 1830
url: /ar/net/aspose.words/editablerange/
---
## EditableRange class

يمثل نطاقًا واحدًا قابلًا للتحرير.

لمعرفة المزيد، قم بزيارة[نموذج كائن المستند (DOM) في Aspose.Words](https://docs.aspose.com/words/net/aspose-words-document-object-model/) مقالة توثيقية.

```csharp
public class EditableRange
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [EditableRangeEnd](../../aspose.words/editablerange/editablerangeend/) { get; } | يحصل على العقدة التي تمثل نهاية النطاق القابل للتحرير. |
| [EditableRangeStart](../../aspose.words/editablerange/editablerangestart/) { get; } | يحصل على العقدة التي تمثل بداية النطاق القابل للتحرير. |
| [EditorGroup](../../aspose.words/editablerange/editorgroup/) { get; set; } | يعيد أو يعين اسمًا مستعارًا (أو مجموعة تحرير) سيتم استخدامه لتحديد ما إذا كان المستخدم الحالي مسموحًا له بتحرير هذا النطاق القابل للتحرير. |
| [Id](../../aspose.words/editablerange/id/) { get; } | يحصل على معرف النطاق القابل للتحرير. |
| [SingleUser](../../aspose.words/editablerange/singleuser/) { get; set; } | يعيد أو يعين المستخدم الفردي للنطاق القابل للتحرير. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Remove](../../aspose.words/editablerange/remove/)() | يزيل النطاق القابل للتحرير من المستند. لا يزيل المحتوى داخله. |

## ملاحظات

`EditableRange` هو كائن "واجهة" يغلف عقدتين[`EditableRangeStart`](./editablerangestart/) و[`EditableRangeEnd`](./editablerangeend/) في شجرة المستندات وتسمح بالعمل مع نطاق قابل للتحرير ككائن واحد.

## أمثلة

يوضح كيفية العمل مع نطاق قابل للتحرير.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "MyPassword");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! Since we have set the document's protection level to read-only," +
                " we cannot edit this paragraph without the password.");

// تسمح لنا النطاقات القابلة للتحرير بترك أجزاء من المستندات المحمية مفتوحة للتحرير.
EditableRangeStart editableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph is inside an editable range, and can be edited.");
EditableRangeEnd editableRangeEnd = builder.EndEditableRange();

//يحتوي النطاق القابل للتحرير ذو التكوين الجيد على عقدة بداية وعقدة نهاية.
// تحتوي هذه العقد على معرفات متطابقة وتشمل عقدًا قابلة للتعديل.
EditableRange editableRange = editableRangeStart.EditableRange;

Assert.AreEqual(editableRangeStart.Id, editableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.Id);

// ترتبط أجزاء مختلفة من النطاق القابل للتحرير ببعضها البعض.
Assert.AreEqual(editableRangeStart.Id, editableRange.EditableRangeStart.Id);
Assert.AreEqual(editableRangeStart.Id, editableRangeEnd.EditableRangeStart.Id);
Assert.AreEqual(editableRange.Id, editableRangeStart.EditableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.EditableRangeEnd.Id);

// يمكننا الوصول إلى أنواع العقد لكل جزء كما يلي. النطاق القابل للتحرير ليس عقدة بحد ذاته.
// ولكن كيان يتكون من بداية ونهاية ومحتوياتهما المغلقة.
Assert.AreEqual(NodeType.EditableRangeStart, editableRangeStart.NodeType);
Assert.AreEqual(NodeType.EditableRangeEnd, editableRangeEnd.NodeType);

builder.Writeln("This paragraph is outside the editable range, and cannot be edited.");

doc.Save(ArtifactsDir + "EditableRange.CreateAndRemove.docx");

// إزالة نطاق قابل للتعديل. ستبقى جميع العقد الموجودة داخل النطاق سليمة.
editableRange.Remove();
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

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
