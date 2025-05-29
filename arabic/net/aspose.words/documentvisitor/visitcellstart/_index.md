---
title: DocumentVisitor.VisitCellStart
linktitle: VisitCellStart
articleTitle: VisitCellStart
second_title: Aspose.Words لـ .NET
description: اكتشف دالة VisitCellStart في DocumentVisitor، وهي أساسية لإدارة تعداد خلايا الجدول بكفاءة. طوّر مهاراتك البرمجية اليوم!
type: docs
weight: 90
url: /ar/net/aspose.words/documentvisitor/visitcellstart/
---
## DocumentVisitor.VisitCellStart method

يتم استدعاؤها عند بدء تعداد خلايا الجدول.

```csharp
public virtual VisitorAction VisitCellStart(Cell cell)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| cell | Cell | الشيء الذي يتم زيارته. |

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

### أنظر أيضا

* enum [VisitorAction](../../visitoraction/)
* class [Cell](../../../aspose.words.tables/cell/)
* class [DocumentVisitor](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
