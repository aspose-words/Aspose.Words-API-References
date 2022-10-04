---
title: EditableRange
second_title: Aspose.Words لمراجع .NET API
description: يمثل نطاقًا واحدًا قابلاً للتحرير .
type: docs
weight: 1270
url: /ar/net/aspose.words/editablerange/
---
## EditableRange class

يمثل نطاقًا واحدًا قابلاً للتحرير .

```csharp
public class EditableRange
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [EditableRangeEnd](../../aspose.words/editablerange/editablerangeend/) { get; } | يحصل على العقدة التي تمثل نهاية النطاق القابل للتحرير. |
| [EditableRangeStart](../../aspose.words/editablerange/editablerangestart/) { get; } | يحصل على العقدة التي تمثل بداية النطاق القابل للتحرير. |
| [EditorGroup](../../aspose.words/editablerange/editorgroup/) { get; set; } | إرجاع أو تعيين الاسم المستعار (أو مجموعة التحرير) التي يجب استخدامها لتحديد ما إذا كان المستخدم الحالي مسموحًا به لتحرير هذا النطاق القابل للتحرير. |
| [Id](../../aspose.words/editablerange/id/) { get; } | الحصول على معرف النطاق القابل للتحرير. |
| [SingleUser](../../aspose.words/editablerange/singleuser/) { get; set; } | إرجاع أو تعيين المستخدم الفردي للنطاق القابل للتحرير. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Remove](../../aspose.words/editablerange/remove/)() | يزيل النطاق القابل للتحرير من المستند. لا يزيل المحتوى داخل النطاق القابل للتحرير. |

### ملاحظات

[`EditableRange`](./editablerange/) هو كائن "واجهة" يغلف عقدتين[`EditableRangeStart`](./editablerangestart/) و[`EditableRangeEnd`](./editablerangeend/) في شجرة المستندات ويسمح بالعمل مع نطاق قابل للتحرير ككائن واحد.

### أمثلة

يوضح كيفية العمل بنطاق قابل للتحرير.

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

// يحتوي النطاق القابل للتعديل جيدًا على عقدة البداية ونقطة النهاية.
// هذه العقد لها معرّفات متطابقة وتشمل عقدًا قابلة للتحرير.
EditableRange editableRange = editableRangeStart.EditableRange;

Assert.AreEqual(editableRangeStart.Id, editableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.Id);

// ترتبط أجزاء مختلفة من النطاق القابل للتعديل ببعضها البعض.
Assert.AreEqual(editableRangeStart.Id, editableRange.EditableRangeStart.Id);
Assert.AreEqual(editableRangeStart.Id, editableRangeEnd.EditableRangeStart.Id);
Assert.AreEqual(editableRange.Id, editableRangeStart.EditableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.EditableRangeEnd.Id);

// يمكننا الوصول إلى أنواع العقدة لكل جزء مثل هذا. النطاق القابل للتحرير في حد ذاته ليس عقدة ،
// ولكن كيان يتكون من بداية ونهاية ومحتوياتها المرفقة.
Assert.AreEqual(NodeType.EditableRangeStart, editableRangeStart.NodeType);
Assert.AreEqual(NodeType.EditableRangeEnd, editableRangeEnd.NodeType);

builder.Writeln("This paragraph is outside the editable range, and cannot be edited.");

doc.Save(ArtifactsDir + "EditableRange.CreateAndRemove.docx");

// إزالة نطاق قابل للتحرير. ستبقى جميع العقد التي كانت داخل النطاق سليمة.
editableRange.Remove();
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

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
