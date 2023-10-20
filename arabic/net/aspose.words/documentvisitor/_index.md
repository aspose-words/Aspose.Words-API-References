---
title: DocumentVisitor Class
linktitle: DocumentVisitor
articleTitle: DocumentVisitor
second_title: Aspose.Words لـ .NET
description: Aspose.Words.DocumentVisitor فصل. الفئة الأساسية لزوار المستندات المخصصة في C#.
type: docs
weight: 470
url: /ar/net/aspose.words/documentvisitor/
---
## DocumentVisitor class

الفئة الأساسية لزوار المستندات المخصصة.

لمعرفة المزيد، قم بزيارة[نموذج كائن مستند Aspose.Words (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) مقالة توثيقية.

```csharp
public abstract class DocumentVisitor
```

## طُرق

| اسم | وصف |
| --- | --- |
| virtual [VisitAbsolutePositionTab](../../aspose.words/documentvisitor/visitabsolutepositiontab/)(*[AbsolutePositionTab](../absolutepositiontab/)*) | تم الاتصال به عندما أ[`AbsolutePositionTab`](../absolutepositiontab/) تمت مصادفة عقدة في المستند. |
| virtual [VisitBodyEnd](../../aspose.words/documentvisitor/visitbodyend/)(*[Body](../body/)*) | يتم استدعاؤه عند انتهاء تعداد القصة النصية الرئيسية في القسم. |
| virtual [VisitBodyStart](../../aspose.words/documentvisitor/visitbodystart/)(*[Body](../body/)*) | يتم استدعاؤه عند بدء تعداد القصة النصية الرئيسية في القسم. |
| virtual [VisitBookmarkEnd](../../aspose.words/documentvisitor/visitbookmarkend/)(*[BookmarkEnd](../bookmarkend/)*) | يتم استدعاؤه عند مواجهة نهاية الإشارة المرجعية في المستند. |
| virtual [VisitBookmarkStart](../../aspose.words/documentvisitor/visitbookmarkstart/)(*[BookmarkStart](../bookmarkstart/)*) | يتم استدعاؤه عند مواجهة بداية إشارة مرجعية في المستند. |
| virtual [VisitBuildingBlockEnd](../../aspose.words/documentvisitor/visitbuildingblockend/)(*[BuildingBlock](../../aspose.words.buildingblocks/buildingblock/)*) | يتم استدعاؤه عند انتهاء تعداد الكتلة البرمجية الإنشائية. |
| virtual [VisitBuildingBlockStart](../../aspose.words/documentvisitor/visitbuildingblockstart/)(*[BuildingBlock](../../aspose.words.buildingblocks/buildingblock/)*) | يتم استدعاؤه عند بدء تعداد الكتلة البرمجية الإنشائية. |
| virtual [VisitCellEnd](../../aspose.words/documentvisitor/visitcellend/)(*[Cell](../../aspose.words.tables/cell/)*) | يتم استدعاؤه عند انتهاء تعداد خلية الجدول. |
| virtual [VisitCellStart](../../aspose.words/documentvisitor/visitcellstart/)(*[Cell](../../aspose.words.tables/cell/)*) | يتم استدعاؤه عند بدء تعداد خلية الجدول. |
| virtual [VisitCommentEnd](../../aspose.words/documentvisitor/visitcommentend/)(*[Comment](../comment/)*) | يتم الاتصال به عند انتهاء تعداد نص التعليق. |
| virtual [VisitCommentRangeEnd](../../aspose.words/documentvisitor/visitcommentrangeend/)(*[CommentRangeEnd](../commentrangeend/)*) | يتم استدعاؤه عند مواجهة نهاية نطاق النص الذي تم التعليق عليه. |
| virtual [VisitCommentRangeStart](../../aspose.words/documentvisitor/visitcommentrangestart/)(*[CommentRangeStart](../commentrangestart/)*) | يتم استدعاؤه عند مواجهة بداية نطاق النص الذي تم التعليق عليه. |
| virtual [VisitCommentStart](../../aspose.words/documentvisitor/visitcommentstart/)(*[Comment](../comment/)*) | يتم الاتصال به عند بدء تعداد نص التعليق. |
| virtual [VisitDocumentEnd](../../aspose.words/documentvisitor/visitdocumentend/)(*[Document](../document/)*) | يتم الاتصال به عند انتهاء تعداد المستند. |
| virtual [VisitDocumentStart](../../aspose.words/documentvisitor/visitdocumentstart/)(*[Document](../document/)*) | يتم الاتصال به عند بدء تعداد المستند. |
| virtual [VisitEditableRangeEnd](../../aspose.words/documentvisitor/visiteditablerangeend/)(*[EditableRangeEnd](../editablerangeend/)*) | يتم استدعاؤه عند مواجهة نهاية نطاق قابل للتحرير في المستند. |
| virtual [VisitEditableRangeStart](../../aspose.words/documentvisitor/visiteditablerangestart/)(*[EditableRangeStart](../editablerangestart/)*) | يتم استدعاؤه عند مواجهة بداية نطاق قابل للتحرير في المستند. |
| virtual [VisitFieldEnd](../../aspose.words/documentvisitor/visitfieldend/)(*[FieldEnd](../../aspose.words.fields/fieldend/)*) | يتم استدعاؤه عندما ينتهي الحقل في المستند. |
| virtual [VisitFieldSeparator](../../aspose.words/documentvisitor/visitfieldseparator/)(*[FieldSeparator](../../aspose.words.fields/fieldseparator/)*) | يتم استدعاؤه عند مواجهة فاصل حقل في المستند. |
| virtual [VisitFieldStart](../../aspose.words/documentvisitor/visitfieldstart/)(*[FieldStart](../../aspose.words.fields/fieldstart/)*) | يتم استدعاؤه عند بدء حقل في المستند. |
| virtual [VisitFootnoteEnd](../../aspose.words/documentvisitor/visitfootnoteend/)(*[Footnote](../../aspose.words.notes/footnote/)*) | يتم استدعاؤه عند انتهاء تعداد نص الحاشية السفلية أو التعليق الختامي. |
| virtual [VisitFootnoteStart](../../aspose.words/documentvisitor/visitfootnotestart/)(*[Footnote](../../aspose.words.notes/footnote/)*) | يتم استدعاؤه عند بدء تعداد نص الحاشية السفلية أو التعليق الختامي. |
| virtual [VisitFormField](../../aspose.words/documentvisitor/visitformfield/)(*[FormField](../../aspose.words.fields/formfield/)*) | يتم استدعاؤه عند مواجهة حقل نموذج في المستند. |
| virtual [VisitGlossaryDocumentEnd](../../aspose.words/documentvisitor/visitglossarydocumentend/)(*[GlossaryDocument](../../aspose.words.buildingblocks/glossarydocument/)*) | يتم استدعاؤه عند انتهاء تعداد مستند المسرد. |
| virtual [VisitGlossaryDocumentStart](../../aspose.words/documentvisitor/visitglossarydocumentstart/)(*[GlossaryDocument](../../aspose.words.buildingblocks/glossarydocument/)*) | يتم استدعاؤه عند بدء تعداد مستند المسرد. |
| virtual [VisitGroupShapeEnd](../../aspose.words/documentvisitor/visitgroupshapeend/)(*[GroupShape](../../aspose.words.drawing/groupshape/)*) | يتم استدعاؤه عند انتهاء تعداد شكل المجموعة. |
| virtual [VisitGroupShapeStart](../../aspose.words/documentvisitor/visitgroupshapestart/)(*[GroupShape](../../aspose.words.drawing/groupshape/)*) | يتم استدعاؤه عند بدء تعداد شكل المجموعة. |
| virtual [VisitHeaderFooterEnd](../../aspose.words/documentvisitor/visitheaderfooterend/)(*[HeaderFooter](../headerfooter/)*) | يتم استدعاؤه عند انتهاء تعداد الرأس أو التذييل في القسم. |
| virtual [VisitHeaderFooterStart](../../aspose.words/documentvisitor/visitheaderfooterstart/)(*[HeaderFooter](../headerfooter/)*) | يتم استدعاؤه عند بدء تعداد الرأس أو التذييل في القسم. |
| virtual [VisitOfficeMathEnd](../../aspose.words/documentvisitor/visitofficemathend/)(*[OfficeMath](../../aspose.words.math/officemath/)*) | يتم استدعاؤه عند انتهاء تعداد كائن Office Math. |
| virtual [VisitOfficeMathStart](../../aspose.words/documentvisitor/visitofficemathstart/)(*[OfficeMath](../../aspose.words.math/officemath/)*) | يتم استدعاؤه عند بدء تعداد كائن Office Math. |
| virtual [VisitParagraphEnd](../../aspose.words/documentvisitor/visitparagraphend/)(*[Paragraph](../paragraph/)*) | يتم استدعاؤه عند انتهاء تعداد الفقرة. |
| virtual [VisitParagraphStart](../../aspose.words/documentvisitor/visitparagraphstart/)(*[Paragraph](../paragraph/)*) | يتم استدعاؤه عند بدء تعداد الفقرة. |
| virtual [VisitRowEnd](../../aspose.words/documentvisitor/visitrowend/)(*[Row](../../aspose.words.tables/row/)*) | يتم استدعاؤه عند انتهاء تعداد صف الجدول. |
| virtual [VisitRowStart](../../aspose.words/documentvisitor/visitrowstart/)(*[Row](../../aspose.words.tables/row/)*) | يتم استدعاؤه عند بدء تعداد صف الجدول. |
| virtual [VisitRun](../../aspose.words/documentvisitor/visitrun/)(*[Run](../run/)*) | يتم الاتصال به عند مواجهة سلسلة من النص في. |
| virtual [VisitSectionEnd](../../aspose.words/documentvisitor/visitsectionend/)(*[Section](../section/)*) | يتم استدعاؤه عند انتهاء تعداد القسم. |
| virtual [VisitSectionStart](../../aspose.words/documentvisitor/visitsectionstart/)(*[Section](../section/)*) | يتم استدعاؤه عند بدء تعداد القسم. |
| virtual [VisitShapeEnd](../../aspose.words/documentvisitor/visitshapeend/)(*[Shape](../../aspose.words.drawing/shape/)*) | يتم استدعاؤه عند انتهاء تعداد الشكل. |
| virtual [VisitShapeStart](../../aspose.words/documentvisitor/visitshapestart/)(*[Shape](../../aspose.words.drawing/shape/)*) | يتم استدعاؤه عند بدء تعداد الشكل. |
| virtual [VisitSmartTagEnd](../../aspose.words/documentvisitor/visitsmarttagend/)(*[SmartTag](../../aspose.words.markup/smarttag/)*) | يتم الاتصال به عند انتهاء تعداد العلامة الذكية. |
| virtual [VisitSmartTagStart](../../aspose.words/documentvisitor/visitsmarttagstart/)(*[SmartTag](../../aspose.words.markup/smarttag/)*) | يتم الاتصال به عند بدء تعداد العلامة الذكية. |
| virtual [VisitSpecialChar](../../aspose.words/documentvisitor/visitspecialchar/)(*[SpecialChar](../specialchar/)*) | تم الاتصال به عندما أ[`SpecialChar`](../specialchar/) تمت مصادفة عقدة في المستند. |
| virtual [VisitStructuredDocumentTagEnd](../../aspose.words/documentvisitor/visitstructureddocumenttagend/)(*[StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/)*) | يتم استدعاؤه عند انتهاء تعداد علامة المستند المنظمة. |
| virtual [VisitStructuredDocumentTagRangeEnd](../../aspose.words/documentvisitor/visitstructureddocumenttagrangeend/)(*[StructuredDocumentTagRangeEnd](../../aspose.words.markup/structureddocumenttagrangeend/)*) | يتم استدعاؤه عند مواجهة StructuredDocumentTagRangeEnd. |
| virtual [VisitStructuredDocumentTagRangeStart](../../aspose.words/documentvisitor/visitstructureddocumenttagrangestart/)(*[StructuredDocumentTagRangeStart](../../aspose.words.markup/structureddocumenttagrangestart/)*) | يتم استدعاؤه عند مواجهة StructuredDocumentTagRangeStart. |
| virtual [VisitStructuredDocumentTagStart](../../aspose.words/documentvisitor/visitstructureddocumenttagstart/)(*[StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/)*) | يتم استدعاؤه عند بدء تعداد علامة المستند المنظمة. |
| virtual [VisitSubDocument](../../aspose.words/documentvisitor/visitsubdocument/)(*[SubDocument](../subdocument/)*) | يتم الاتصال به عند مواجهة مستند فرعي. |
| virtual [VisitTableEnd](../../aspose.words/documentvisitor/visittableend/)(*[Table](../../aspose.words.tables/table/)*) | يتم استدعاؤه عند انتهاء تعداد الجدول. |
| virtual [VisitTableStart](../../aspose.words/documentvisitor/visittablestart/)(*[Table](../../aspose.words.tables/table/)*) | يتم استدعاؤه عند بدء تعداد الجدول. |

## ملاحظات

مع`DocumentVisitor` يمكنك تحديد وتنفيذ العمليات المخصصة التي تتطلب التعداد فوق شجرة المستندات.

على سبيل المثال، يستخدم Aspose.Words`DocumentVisitor` داخليا للحفظ[`Document`](../document/) بتنسيقات مختلفة ولعمليات أخرى مثل البحث عن الحقول أو الإشارات المرجعية فوق جزء من المستند.

ليستخدم`DocumentVisitor`:

1. إنشاء فئة مشتقة من`DocumentVisitor`.
2. تجاوز وتوفير تطبيقات لبعض أو كل طرق VisitXXX لتنفيذ بعض العمليات المخصصة.
3. يتصل[`العقدة. قبول`](../node/accept/) على ال[`Node`](../node/) that الذي تريد بدء التعداد منه.

`DocumentVisitor` يوفر تطبيقات افتراضية لجميع أساليب VisitXXX لتسهيل إنشاء زوار مستند جدد حيث يلزم تجاوز الطرق المطلوبة لزائر معين فقط. ليس من الضروري تجاوز كافة أساليب الزائر.

لمزيد من المعلومات، راجع نمط تصميم الزائر.

## أمثلة

يوضح كيفية استخدام زائر المستند لطباعة بنية عقدة المستند.

```csharp
public void DocStructureToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    DocStructurePrinter visitor = new DocStructurePrinter();

    // عندما نحصل على عقدة مركبة لقبول زائر المستند، يقوم الزائر بزيارة العقدة المقبولة،
    // ثم يجتاز جميع أبناء العقدة بطريقة العمق الأول.
    // يمكن للزائر قراءة وتعديل كل عقدة تمت زيارتها.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// يجتاز شجرة العقدة من العقد الفرعية.
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
    /// يتم الاتصال به عند مواجهة عقدة مستند.
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
    /// يتم الاتصال به بعد زيارة جميع العقد التابعة لعقدة المستند.
    /// </summary>
    public override VisitorAction VisitDocumentEnd(Document doc)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Document end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم الاتصال به عند مواجهة عقدة القسم في المستند.
    /// </summary>
    public override VisitorAction VisitSectionStart(Section section)
    {
        // احصل على فهرس قسمنا داخل المستند.
        NodeCollection docSections = section.Document.GetChildNodes(NodeType.Section, false);
        int sectionIndex = docSections.IndexOf(section);

        IndentAndAppendLine("[Section start] Section index: " + sectionIndex);
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم الاتصال به بعد زيارة جميع العقد التابعة لعقدة القسم.
    /// </summary>
    public override VisitorAction VisitSectionEnd(Section section)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Section end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم الاتصال به عند مواجهة عقدة النص في المستند.
    /// </summary>
    public override VisitorAction VisitBodyStart(Body body)
    {
        int paragraphCount = body.Paragraphs.Count;
        IndentAndAppendLine("[Body start] Paragraphs: " + paragraphCount);
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم الاتصال به بعد زيارة جميع العقد التابعة للعقدة الأساسية.
    /// </summary>
    public override VisitorAction VisitBodyEnd(Body body)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Body end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤه عند مواجهة عقدة فقرة في المستند.
    /// </summary>
    public override VisitorAction VisitParagraphStart(Paragraph paragraph)
    {
        IndentAndAppendLine("[Paragraph start]");
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم الاتصال به بعد زيارة جميع العقد التابعة لعقدة الفقرة.
    /// </summary>
    public override VisitorAction VisitParagraphEnd(Paragraph paragraph)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Paragraph end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم الاتصال به عند مواجهة عقدة التشغيل في المستند.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم الاتصال به عند مواجهة عقدة مستند فرعي في المستند.
    /// </summary>
    public override VisitorAction VisitSubDocument(SubDocument subDocument)
    {
        IndentAndAppendLine("[SubDocument]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// ألحق سطرًا بـ StringBuilder وقم بوضع مسافة بادئة له اعتمادًا على مدى عمق الزائر في شجرة المستندات.
    /// </summary>
    /// <param name="text"></param>
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
