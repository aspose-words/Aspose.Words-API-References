---
title: DocumentVisitor
second_title: Aspose.Words لمراجع .NET API
description: الفئة الأساسية لزوار المستند المخصص.
type: docs
weight: 460
url: /ar/net/aspose.words/documentvisitor/
---
## DocumentVisitor class

الفئة الأساسية لزوار المستند المخصص.

```csharp
public abstract class DocumentVisitor
```

## طُرق

| اسم | وصف |
| --- | --- |
| virtual [VisitAbsolutePositionTab](../../aspose.words/documentvisitor/visitabsolutepositiontab/)(AbsolutePositionTab) | عند استدعائها[`AbsolutePositionTab`](../absolutepositiontab/) تم مصادفة العقدة في المستند. |
| virtual [VisitBodyEnd](../../aspose.words/documentvisitor/visitbodyend/)(Body) | يتم الاستدعاء عند انتهاء تعداد القصة النصية الرئيسية في أحد الأقسام. |
| virtual [VisitBodyStart](../../aspose.words/documentvisitor/visitbodystart/)(Body) | يتم الاستدعاء عند بدء تعداد القصة النصية الرئيسية في أحد الأقسام. |
| virtual [VisitBookmarkEnd](../../aspose.words/documentvisitor/visitbookmarkend/)(BookmarkEnd) | يتم استدعاؤه عند مواجهة نهاية إشارة مرجعية في المستند. |
| virtual [VisitBookmarkStart](../../aspose.words/documentvisitor/visitbookmarkstart/)(BookmarkStart) | يتم الاتصال به عند مواجهة بداية إشارة مرجعية في المستند. |
| virtual [VisitBuildingBlockEnd](../../aspose.words/documentvisitor/visitbuildingblockend/)(BuildingBlock) | يتم استدعاؤه عند انتهاء تعداد الكتلة البرمجية الإنشائية . |
| virtual [VisitBuildingBlockStart](../../aspose.words/documentvisitor/visitbuildingblockstart/)(BuildingBlock) | يتم استدعاؤه عند بدء تعداد الكتلة البرمجية الإنشائية . |
| virtual [VisitCellEnd](../../aspose.words/documentvisitor/visitcellend/)(Cell) | يتم استدعاؤها عند انتهاء تعداد خلية جدول . |
| virtual [VisitCellStart](../../aspose.words/documentvisitor/visitcellstart/)(Cell) | يتم استدعاؤها عند بدء تعداد خلية جدول . |
| virtual [VisitCommentEnd](../../aspose.words/documentvisitor/visitcommentend/)(Comment) | يتم الاستدعاء عند انتهاء تعداد نص التعليق. |
| virtual [VisitCommentRangeEnd](../../aspose.words/documentvisitor/visitcommentrangeend/)(CommentRangeEnd) | يتم استدعاؤه عند مواجهة نهاية نطاق النص المعلق عليه . |
| virtual [VisitCommentRangeStart](../../aspose.words/documentvisitor/visitcommentrangestart/)(CommentRangeStart) | يتم استدعاؤه عند مواجهة بداية نطاق النص المعلق عليه . |
| virtual [VisitCommentStart](../../aspose.words/documentvisitor/visitcommentstart/)(Comment) | يتم الاستدعاء عند بدء تعداد نص التعليق. |
| virtual [VisitDocumentEnd](../../aspose.words/documentvisitor/visitdocumentend/)(Document) | يتم استدعاؤها عند انتهاء تعداد المستند. |
| virtual [VisitDocumentStart](../../aspose.words/documentvisitor/visitdocumentstart/)(Document) | يتم استدعاؤها عند بدء تعداد المستند. |
| virtual [VisitEditableRangeEnd](../../aspose.words/documentvisitor/visiteditablerangeend/)(EditableRangeEnd) | يتم استدعاؤه عند مواجهة نهاية نطاق قابل للتحرير في المستند. |
| virtual [VisitEditableRangeStart](../../aspose.words/documentvisitor/visiteditablerangestart/)(EditableRangeStart) | يتم استدعاؤها عند مواجهة بداية نطاق قابل للتحرير في المستند. |
| virtual [VisitFieldEnd](../../aspose.words/documentvisitor/visitfieldend/)(FieldEnd) | يتم استدعائها عند انتهاء أحد الحقول في المستند. |
| virtual [VisitFieldSeparator](../../aspose.words/documentvisitor/visitfieldseparator/)(FieldSeparator) | يتم استدعاؤه عند مصادفة فاصل حقل في المستند. |
| virtual [VisitFieldStart](../../aspose.words/documentvisitor/visitfieldstart/)(FieldStart) | يتم استدعاؤها عندما يبدأ أحد الحقول في المستند. |
| virtual [VisitFootnoteEnd](../../aspose.words/documentvisitor/visitfootnoteend/)(Footnote) | يتم استدعاؤها عند انتهاء تعداد نص حاشية سفلية أو تعليق ختامي. |
| virtual [VisitFootnoteStart](../../aspose.words/documentvisitor/visitfootnotestart/)(Footnote) | يتم الاستدعاء عند بدء تعداد نص حاشية سفلية أو تعليق ختامي. |
| virtual [VisitFormField](../../aspose.words/documentvisitor/visitformfield/)(FormField) | يتم استدعاؤه عند مواجهة حقل نموذج في المستند. |
| virtual [VisitGlossaryDocumentEnd](../../aspose.words/documentvisitor/visitglossarydocumentend/)(GlossaryDocument) | يتم استدعاؤه عند انتهاء تعداد مستند مسرد المصطلحات. |
| virtual [VisitGlossaryDocumentStart](../../aspose.words/documentvisitor/visitglossarydocumentstart/)(GlossaryDocument) | يتم استدعاؤه عند بدء تعداد مستند مسرد المصطلحات. |
| virtual [VisitGroupShapeEnd](../../aspose.words/documentvisitor/visitgroupshapeend/)(GroupShape) | يتم استدعاؤها عند انتهاء تعداد شكل مجموعة . |
| virtual [VisitGroupShapeStart](../../aspose.words/documentvisitor/visitgroupshapestart/)(GroupShape) | يتم استدعاؤها عند بدء تعداد شكل مجموعة . |
| virtual [VisitHeaderFooterEnd](../../aspose.words/documentvisitor/visitheaderfooterend/)(HeaderFooter) | يتم استدعاؤه عند انتهاء تعداد رأس أو تذييل في قسم. |
| virtual [VisitHeaderFooterStart](../../aspose.words/documentvisitor/visitheaderfooterstart/)(HeaderFooter) | يتم استدعاؤه عند بدء تعداد رأس أو تذييل في أحد الأقسام. |
| virtual [VisitOfficeMathEnd](../../aspose.words/documentvisitor/visitofficemathend/)(OfficeMath) | يتم استدعاؤه عند انتهاء تعداد كائن Office Math . |
| virtual [VisitOfficeMathStart](../../aspose.words/documentvisitor/visitofficemathstart/)(OfficeMath) | يتم استدعاؤه عند بدء تعداد كائن Office Math . |
| virtual [VisitParagraphEnd](../../aspose.words/documentvisitor/visitparagraphend/)(Paragraph) | يتم استدعاؤها عند انتهاء تعداد فقرة. |
| virtual [VisitParagraphStart](../../aspose.words/documentvisitor/visitparagraphstart/)(Paragraph) | يتم استدعاؤها عند بدء تعداد فقرة. |
| virtual [VisitRowEnd](../../aspose.words/documentvisitor/visitrowend/)(Row) | يتم استدعاؤه عند انتهاء تعداد صف جدول . |
| virtual [VisitRowStart](../../aspose.words/documentvisitor/visitrowstart/)(Row) | يتم استدعاؤه عند بدء تعداد صف جدول . |
| virtual [VisitRun](../../aspose.words/documentvisitor/visitrun/)(Run) | يتم استدعاؤه عند مصادفة تشغيل نص في . |
| virtual [VisitSectionEnd](../../aspose.words/documentvisitor/visitsectionend/)(Section) | يتم استدعاؤه عند انتهاء تعداد القسم. |
| virtual [VisitSectionStart](../../aspose.words/documentvisitor/visitsectionstart/)(Section) | يتم استدعاؤه عند بدء تعداد القسم . |
| virtual [VisitShapeEnd](../../aspose.words/documentvisitor/visitshapeend/)(Shape) | يتم استدعاؤها عند انتهاء تعداد الشكل. |
| virtual [VisitShapeStart](../../aspose.words/documentvisitor/visitshapestart/)(Shape) | يتم استدعاؤها عند بدء تعداد الشكل. |
| virtual [VisitSmartTagEnd](../../aspose.words/documentvisitor/visitsmarttagend/)(SmartTag) | يتم الاستدعاء عند انتهاء تعداد العلامة الذكية . |
| virtual [VisitSmartTagStart](../../aspose.words/documentvisitor/visitsmarttagstart/)(SmartTag) | يتم الاستدعاء عند بدء تعداد علامة ذكية . |
| virtual [VisitSpecialChar](../../aspose.words/documentvisitor/visitspecialchar/)(SpecialChar) | عند استدعائها[`SpecialChar`](../specialchar/) تم مصادفة العقدة في المستند. |
| virtual [VisitStructuredDocumentTagEnd](../../aspose.words/documentvisitor/visitstructureddocumenttagend/)(StructuredDocumentTag) | يتم استدعاؤها عند انتهاء تعداد علامة مستند منظم. |
| virtual [VisitStructuredDocumentTagRangeEnd](../../aspose.words/documentvisitor/visitstructureddocumenttagrangeend/)(StructuredDocumentTagRangeEnd) |  |
| virtual [VisitStructuredDocumentTagRangeStart](../../aspose.words/documentvisitor/visitstructureddocumenttagrangestart/)(StructuredDocumentTagRangeStart) |  |
| virtual [VisitStructuredDocumentTagStart](../../aspose.words/documentvisitor/visitstructureddocumenttagstart/)(StructuredDocumentTag) | يتم استدعاؤها عند بدء تعداد علامة مستند منظم. |
| virtual [VisitSubDocument](../../aspose.words/documentvisitor/visitsubdocument/)(SubDocument) | يتم استدعاؤه عند مصادفة مستند ثانوي . |
| virtual [VisitTableEnd](../../aspose.words/documentvisitor/visittableend/)(Table) | يتم استدعاؤه عند انتهاء تعداد جدول . |
| virtual [VisitTableStart](../../aspose.words/documentvisitor/visittablestart/)(Table) | يتم استدعاؤها عند بدء تعداد جدول . |

### ملاحظات

مع **وثيقة الزائر** يمكنك تحديد وتنفيذ عمليات مخصصة_ التي تتطلب تعدادًا عبر شجرة المستند.

على سبيل المثال ، يستخدم Aspose.Words **وثيقة الزائر** داخليا للحفظ **وثيقة** بتنسيقات مختلفة ولعمليات أخرى مثل البحث عن الحقول أو الإشارات المرجعية over جزء من المستند.

ليستخدم **وثيقة الزائر**:

1. قم بإنشاء فئة مشتقة من **وثيقة الزائر**.
2. تجاوز وتوفير تطبيقات لبعض أو كل أساليب VisitXXX لإجراء بعض العمليات المخصصة.
3. مكالمة[`العقدة قبول`](../node/accept/) على ال **العقدة** that الذي تريد بدء التعداد منه.

**وثيقة الزائر**يوفر عمليات التنفيذ الافتراضية لجميع طرق VisitXXX لتسهيل إنشاء زوار مستند جديد حيث يجب تجاوز الطرق المطلوبة فقط للزائر المعين. ليس من الضروري تجاوز كل طرق الزائر.

لمزيد من المعلومات ، راجع نمط تصميم الزائر.

### أمثلة

يوضح كيفية استخدام زائر المستند لطباعة بنية عقدة المستند.

```csharp
public void DocStructureToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    DocStructurePrinter visitor = new DocStructurePrinter();

    // عندما نحصل على عقدة مركبة لقبول زائر المستند ، يزور الزائر عقدة القبول ،
    // ثم يعبر جميع أبناء العقدة بطريقة العمق أولاً.
    // يمكن للزائر قراءة كل عقدة تمت زيارتها وتعديلها.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// يتجاوز شجرة العقد التابعة للعقد.
/// ينشئ خريطة لهذه الشجرة على شكل سلسلة.
/// </summary>
public class DocStructurePrinter : DocumentVisitor
{
    public DocStructurePrinter()
    {
        mAcceptingNodeChildTree = new StringBuilder();
    }

    public string GetText()
    {
        return mAcceptingNodeChildTree.ToString();
    }

    /// <summary>
    /// يتم الاستدعاء عند مصادفة عقدة المستند.
    /// </summary>
    public override VisitorAction VisitDocumentStart(Document doc)
    {
        int childNodeCount = doc.GetChildNodes(NodeType.Any, true).Count;

        IndentAndAppendLine("[Document start] Child nodes: " + childNodeCount);
        mDocTraversalDepth++;

        // السماح للزائر بمواصلة زيارة العقد الأخرى.
        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها بعد زيارة جميع العقد الفرعية لعقدة المستند.
    /// </summary>
    public override VisitorAction VisitDocumentEnd(Document doc)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Document end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند مواجهة عقدة قسم في المستند.
    /// </summary>
    public override VisitorAction VisitSectionStart(Section section)
    {
        // احصل على فهرس القسم الخاص بنا داخل المستند.
        NodeCollection docSections = section.Document.GetChildNodes(NodeType.Section, false);
        int sectionIndex = docSections.IndexOf(section);

        IndentAndAppendLine("[Section start] Section index: " + sectionIndex);
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها بعد زيارة جميع العقد الفرعية لعقدة القسم.
    /// </summary>
    public override VisitorAction VisitSectionEnd(Section section)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Section end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند مصادفة عقدة أساسية في المستند.
    /// </summary>
    public override VisitorAction VisitBodyStart(Body body)
    {
        int paragraphCount = body.Paragraphs.Count;
        IndentAndAppendLine("[Body start] Paragraphs: " + paragraphCount);
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها بعد زيارة جميع العقد الفرعية لعقدة الجسم.
    /// </summary>
    public override VisitorAction VisitBodyEnd(Body body)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Body end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند مواجهة عقدة فقرة في المستند.
    /// </summary>
    public override VisitorAction VisitParagraphStart(Paragraph paragraph)
    {
        IndentAndAppendLine("[Paragraph start]");
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها بعد زيارة جميع العقد الفرعية لعقدة فقرة.
    /// </summary>
    public override VisitorAction VisitParagraphEnd(Paragraph paragraph)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Paragraph end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم الاستدعاء عند مواجهة عقدة تشغيل في المستند.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤه عند مواجهة عقدة SubDocument في المستند.
    /// </summary>
    public override VisitorAction VisitSubDocument(SubDocument subDocument)
    {
        IndentAndAppendLine("[SubDocument]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// قم بإلحاق سطر بـ StringBuilder وقم بعمل مسافة بادئة له اعتمادًا على مدى عمق الزائر في شجرة المستند.
    /// </summary>
    /// < param name = "text" > < / param >
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++) mAcceptingNodeChildTree.Append("|  ");

        mAcceptingNodeChildTree.AppendLine(text);
    }

    private int mDocTraversalDepth;
    private readonly StringBuilder mAcceptingNodeChildTree;
}
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
