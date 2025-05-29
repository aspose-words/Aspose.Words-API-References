---
title: DocumentVisitor.VisitTableEnd
linktitle: VisitTableEnd
articleTitle: VisitTableEnd
second_title: Aspose.Words لـ .NET
description: استكشف طريقة DocumentVisitor VisitTableEnd، التي تشير بشكل فعال إلى نهاية تعداد الجدول، مما يعزز تجربة الترميز الخاصة بك.
type: docs
weight: 490
url: /ar/net/aspose.words/documentvisitor/visittableend/
---
## DocumentVisitor.VisitTableEnd method

يتم استدعاؤها عند انتهاء تعداد الجدول.

```csharp
public virtual VisitorAction VisitTableEnd(Table table)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| table | Table | الشيء الذي يتم زيارته. |

### قيمة الإرجاع

أ[`VisitorAction`](../../visitoraction/) القيمة التي تحدد كيفية مواصلة التعداد.

## أمثلة

يوضح كيفية طباعة بنية العقدة لكل جدول في المستند.

```csharp
public void TableToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    TableStructurePrinter visitor = new TableStructurePrinter();

    // عندما نحصل على عقدة مركبة لقبول زائر مستند، يقوم الزائر بزيارة العقدة المستقبلة،
    // ثم يمر عبر جميع أبناء العقدة بطريقة العمق أولاً.
    //يمكن للزائر قراءة وتعديل كل عقدة تمت زيارتها.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// يجتاز شجرة العقد غير الثنائية المكونة من عقد فرعية.
/// إنشاء خريطة في شكل سلسلة من جميع عقد الجدول التي تم مواجهتها وأطفالها.
/// </summary>
public class TableStructurePrinter : DocumentVisitor
{
    public TableStructurePrinter()
    {
        mVisitedTables = new StringBuilder();
        mVisitorIsInsideTable = false;
    }

    public string GetText()
    {
        return mVisitedTables.ToString();
    }

    /// <summary>
    /// يتم استدعاؤها عند مواجهة عقدة تشغيل في المستند.
    /// لن يتم تسجيل عمليات التشغيل التي لا تقع ضمن الجداول.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideTable) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند العثور على جدول في المستند.
    /// </summary>
    public override VisitorAction VisitTableStart(Table table)
    {
        int rows = 0;
        int columns = 0;

        if (table.Rows.Count > 0)
        {
            rows = table.Rows.Count;
            columns = table.FirstRow.Count;
        }

        IndentAndAppendLine("[Table start] Size: " + rows + "x" + columns);
        mDocTraversalDepth++;
        mVisitorIsInsideTable = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها بعد زيارة جميع العقد الفرعية لعقدة الجدول.
    /// </summary>
    public override VisitorAction VisitTableEnd(Table table)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Table end]");
        mVisitorIsInsideTable = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند مواجهة عقدة صف في المستند.
    /// </summary>
    public override VisitorAction VisitRowStart(Row row)
    {
        string rowContents = row.GetText().TrimEnd(new []{ '\u0007', ' ' }).Replace("\u0007", ", ");
        int rowWidth = row.IndexOf(row.LastCell) + 1;
        int rowIndex = row.ParentTable.IndexOf(row);
        string rowStatusInTable = row.IsFirstRow && row.IsLastRow ? "only" : row.IsFirstRow ? "first" : row.IsLastRow ? "last" : "";
        if (rowStatusInTable != "")
        {
            rowStatusInTable = $", the {rowStatusInTable} row in this table,";
        }

        IndentAndAppendLine($"[Row start] Row #{++rowIndex}{rowStatusInTable} width {rowWidth}, \"{rowContents}\"");
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها بعد زيارة جميع العقد الفرعية لعقدة الصف.
    /// </summary>
    public override VisitorAction VisitRowEnd(Row row)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Row end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند مواجهة عقدة خلية في المستند.
    /// </summary>
    public override VisitorAction VisitCellStart(Cell cell)
    {
        Row row = cell.ParentRow;
        Table table = row.ParentTable;
        string cellStatusInRow = cell.IsFirstCell && cell.IsLastCell ? "only" : cell.IsFirstCell ? "first" : cell.IsLastCell ? "last" : "";
        if (cellStatusInRow != "")
        {
            cellStatusInRow = $", the {cellStatusInRow} cell in this row";
        }

        IndentAndAppendLine($"[Cell start] Row {table.IndexOf(row) + 1}, Col {row.IndexOf(cell) + 1}{cellStatusInRow}");
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها بعد زيارة جميع العقد الفرعية لعقدة الخلية.
    /// </summary>
    public override VisitorAction VisitCellEnd(Cell cell)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Cell end]");
        return VisitorAction.Continue;
    }

    /// <summary>
    /// أضف سطرًا إلى StringBuilder، وقم بتدويره حسب عمق الزائر
    /// في شجرة العقد الفرعية للجدول الحالي.
    /// </summary>
    /// <اسم المعلمة="نص"></param>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++)
        {
            mVisitedTables.Append("|  ");
        }

        mVisitedTables.AppendLine(text);
    }

    private bool mVisitorIsInsideTable;
    private int mDocTraversalDepth;
    private readonly StringBuilder mVisitedTables;
}
```

يوضح كيفية استخدام تنفيذ DocumentVisitor لإزالة كل المحتوى المخفي من المستند.

```csharp
public void RemoveHiddenContentFromDocument()
{
    Document doc = new Document(MyDir + "Hidden content.docx");
    RemoveHiddenContentVisitor hiddenContentRemover = new RemoveHiddenContentVisitor();

    // فيما يلي ثلاثة أنواع من الحقول التي يمكنها قبول زائر المستند،
    // مما سيسمح لها بزيارة العقدة المستقبلة، ثم عبور العقد الفرعية الخاصة بها بطريقة العمق أولاً.
    // 1 - عقدة الفقرة:
    Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 4, true);
    para.Accept(hiddenContentRemover);

    // 2 - عقدة الجدول:
    Table table = doc.FirstSection.Body.Tables[0];
    table.Accept(hiddenContentRemover);

    // 3 - عقدة المستند:
    doc.Accept(hiddenContentRemover);

    doc.Save(ArtifactsDir + "Font.RemoveHiddenContentFromDocument.docx");
}

/// <summary>
/// يقوم بإزالة جميع العقد التي تمت زيارتها والتي تم وضع علامة "المحتوى المخفي" عليها.
/// </summary>
public class RemoveHiddenContentVisitor : DocumentVisitor
{
    /// <summary>
    /// يتم استدعاؤها عند مواجهة عقدة FieldStart في المستند.
    /// </summary>
    public override VisitorAction VisitFieldStart(FieldStart fieldStart)
    {
        if (fieldStart.Font.Hidden)
            fieldStart.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند مواجهة عقدة FieldEnd في المستند.
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        if (fieldEnd.Font.Hidden)
            fieldEnd.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند مواجهة عقدة FieldSeparator في المستند.
    /// </summary>
    public override VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
    {
        if (fieldSeparator.Font.Hidden)
            fieldSeparator.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند مواجهة عقدة تشغيل في المستند.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (run.Font.Hidden)
            run.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند مواجهة عقدة فقرة في المستند.
    /// </summary>
    public override VisitorAction VisitParagraphStart(Paragraph paragraph)
    {
        if (paragraph.ParagraphBreakFont.Hidden)
            paragraph.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند العثور على FormField في المستند.
    /// </summary>
    public override VisitorAction VisitFormField(FormField formField)
    {
        if (formField.Font.Hidden)
            formField.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند مواجهة GroupShape في المستند.
    /// </summary>
    public override VisitorAction VisitGroupShapeStart(GroupShape groupShape)
    {
        if (groupShape.Font.Hidden)
            groupShape.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند العثور على شكل في المستند.
    /// </summary>
    public override VisitorAction VisitShapeStart(Shape shape)
    {
        if (shape.Font.Hidden)
            shape.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند العثور على تعليق في المستند.
    /// </summary>
    public override VisitorAction VisitCommentStart(Comment comment)
    {
        if (comment.Font.Hidden)
            comment.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند العثور على حاشية سفلية في المستند.
    /// </summary>
    public override VisitorAction VisitFootnoteStart(Footnote footnote)
    {
        if (footnote.Font.Hidden)
            footnote.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند مواجهة SpecialCharacter في المستند.
    /// </summary>
    public override VisitorAction VisitSpecialChar(SpecialChar specialChar)
    {
        Console.WriteLine(specialChar.GetText());

        if (specialChar.Font.Hidden)
            specialChar.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند انتهاء زيارة عقدة الجدول في المستند.
    /// </summary>
    public override VisitorAction VisitTableEnd(Table table)
    {
        // قد يكون المحتوى الموجود داخل خلايا الجدول يحتوي على علامة المحتوى المخفي، ولكن الجداول نفسها لا يمكن أن يكون لديها هذه العلامة.
        // إذا لم يكن في هذا الجدول سوى محتوى مخفي، فإن هذا الزائر كان سيحذفه بالكامل،
        //ولن يتبقى أي عقدة فرعية.
        // وبالتالي، يمكننا أيضًا التعامل مع الجدول نفسه كمحتوى مخفي وإزالته.
        // ستحتوي الجداول الفارغة التي لا تحتوي على محتوى مخفي على خلايا تحتوي على فقرات فارغة بداخلها،
        // والتي لن يقوم هذا الزائر بإزالتها.
        if (!table.HasChildNodes)
            table.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند انتهاء زيارة عقدة الخلية في المستند.
    /// </summary>
    public override VisitorAction VisitCellEnd(Cell cell)
    {
        if (!cell.HasChildNodes && cell.ParentNode != null)
            cell.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند انتهاء زيارة عقدة الصف في المستند.
    /// </summary>
    public override VisitorAction VisitRowEnd(Row row)
    {
        if (!row.HasChildNodes && row.ParentNode != null)
            row.Remove();

        return VisitorAction.Continue;
    }
}
```

### أنظر أيضا

* enum [VisitorAction](../../visitoraction/)
* class [Table](../../../aspose.words.tables/table/)
* class [DocumentVisitor](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
