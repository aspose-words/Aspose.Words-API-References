---
title: AbsolutePositionTab
second_title: Aspose.Words لمراجع .NET API
description: علامة تبويب الموضع المطلق هي حرف يُستخدم لتقديم الموضع على السطر الحالي للنص عند عرض محتوى معالجة Word هذا.
type: docs
weight: 10
url: /ar/net/aspose.words/absolutepositiontab/
---
## AbsolutePositionTab class

علامة تبويب الموضع المطلق هي حرف يُستخدم لتقديم الموضع على السطر الحالي للنص عند عرض محتوى معالجة Word هذا.

```csharp
public class AbsolutePositionTab : SpecialChar
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | يحدد معرف العقدة المخصص ._ x000d_ |
| virtual [Document](../../aspose.words/node/document) { get; } | الحصول على المستند الذي تنتمي إليه هذه العقدة . |
| [Font](../../aspose.words/inline/font) { get; } | يوفر الوصول إلى تنسيق خط هذا الكائن. |
| virtual [IsComposite](../../aspose.words/node/iscomposite) { get; } | إرجاع صحيح إذا كانت هذه العقدة يمكن أن تحتوي على عقد أخرى. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision) { get; } | إرجاع صحيح إذا تم حذف هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision) { get; } | إرجاع صحيح إذا تم تغيير تنسيق الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision) { get; } | إرجاع صحيح إذا تم إدراج هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision) { get; } | عوائد **حقيقي** إذا تم نقل (حذف) هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision) { get; } | عوائد **حقيقي** إذا تم نقل هذا الكائن (إدراجه) في Microsoft Word أثناء تمكين تعقب التغيير. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| override [NodeType](../../aspose.words/specialchar/nodetype) { get; } | عوائد **NodeType.SpecialChar** . |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | الحصول على الأصل المباشر لهذه العقدة. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph) { get; } | استرداد الأصل[`Paragraph`](../paragraph) من هذه العقدة. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرة. |
| [Range](../../aspose.words/node/range) { get; } | إرجاع أ **نطاق** الكائن الذي يمثل جزء المستند الموجود في هذه العقدة. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Accept](../../aspose.words/absolutepositiontab/accept)(DocumentVisitor) | يقبل الزائر . |
| [Clone](../../aspose.words/node/clone)(bool) | لإنشاء نسخة مكررة من العقدة . |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | يحصل على أول سلف محدد[`NodeType`](../nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | الحصول على الأصل الأول لنوع الكائن المحدد. |
| override [GetText](../../aspose.words/specialchar/gettext)() | يحصل على الحرف الخاص الذي تمثله هذه العقدة . |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | الحصول على العقدة التالية وفقًا لخوارزمية اجتياز الشجرة بالطلب المسبق. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | الحصول على العقدة السابقة وفقًا لخوارزمية اجتياز الشجرة بالطلب المسبق. |
| [Remove](../../aspose.words/node/remove)() | يزيل نفسه من الأصل. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | يصدر محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | يصدر محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |

### أمثلة

يوضح كيفية معالجة أحرف علامة تبويب الموضع المطلق مع زائر المستند.

```csharp
public void DocumentToTxt()
{
    Document doc = new Document(MyDir + "Absolute position tab.docx");

    // استخراج محتويات النص من وثيقتنا بقبول زائر المستند المخصص هذا.
    DocTextExtractor myDocTextExtractor = new DocTextExtractor();
    doc.FirstSection.Body.Accept(myDocTextExtractor);

    // تم تحويل علامة تبويب الموضع المطلق ، التي ليس لها مكافئ في شكل سلسلة ، بشكل صريح إلى حرف جدولة.
    Assert.AreEqual("Before AbsolutePositionTab\tAfter AbsolutePositionTab", myDocTextExtractor.GetText());

    // يمكن لـ AbsolutePositionTab قبول DocumentVisitor بنفسه أيضًا.
    AbsolutePositionTab absPositionTab = (AbsolutePositionTab)doc.FirstSection.Body.FirstParagraph.GetChild(NodeType.SpecialChar, 0, true);

    myDocTextExtractor = new DocTextExtractor();
    absPositionTab.Accept(myDocTextExtractor);

    Assert.AreEqual("\t", myDocTextExtractor.GetText());
}

/// <summary>
/// يجمع محتويات النص لكل عمليات التشغيل في المستند الذي تمت زيارته. يستبدل كل أحرف الجدولة المطلقة بعلامات جدولة عادية.
/// </summary>
public class DocTextExtractor : DocumentVisitor
{
    public DocTextExtractor()
    {
        mBuilder = new StringBuilder();
    }

    /// <summary>
    /// يتم الاستدعاء عند مواجهة عقدة تشغيل في المستند.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        AppendText(run.Text);
        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند مواجهة عقدة AbsolutePositionTab في المستند.
    /// </summary>
    public override VisitorAction VisitAbsolutePositionTab(AbsolutePositionTab tab)
    {
        mBuilder.Append("\t");
        return VisitorAction.Continue;
    }

    /// <summary>
    /// يضيف نصًا إلى الإخراج الحالي. يكرم علامة الإخراج الممكنة / المعطلة.
    /// </summary>
    private void AppendText(string text)
    {
        mBuilder.Append(text);
    }

    /// <summary>
    /// نص عادي للمستند الذي جمعه الزائر.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    private readonly StringBuilder mBuilder;
}
```

### أنظر أيضا

* class [SpecialChar](../specialchar)
* مساحة الاسم [Aspose.Words](../../aspose.words)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
