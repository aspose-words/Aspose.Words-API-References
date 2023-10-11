---
title: CellFormat.VerticalMerge
second_title: Aspose.Words لمراجع .NET API
description: CellFormat ملكية. يحدد كيفية دمج الخلية مع الخلايا الأخرى عموديًا.
type: docs
weight: 130
url: /ar/net/aspose.words.tables/cellformat/verticalmerge/
---
## CellFormat.VerticalMerge property

يحدد كيفية دمج الخلية مع الخلايا الأخرى عموديًا.

```csharp
public CellMerge VerticalMerge { get; set; }
```

### ملاحظات

لا يمكن دمج الخلايا رأسيًا إلا إذا كانت حدودها اليمنى واليسرى متطابقة.

عندما يتم دمج الخلايا رأسيًا، يتم دمج مساحات العرض للخلايا المدمجة. يتم استخدام المنطقة المدمجة لعرض محتويات الخلية المدمجة رأسيًا الأولى ويجب أن تكون كافة الخلايا الأخرى المدمجة رأسيًا فارغة.

### أمثلة

طباعة نوع الدمج الأفقي والرأسي للخلية.

```csharp
public void CheckCellsMerged()
{
    Document doc = new Document(MyDir + "Table with merged cells.docx");
    Table table = doc.FirstSection.Body.Tables[0];

    foreach (Row row in table.Rows.OfType<Row>())
        foreach (Cell cell in row.Cells.OfType<Cell>())
            Console.WriteLine(PrintCellMergeType(cell));
}

public string PrintCellMergeType(Cell cell)
{
    bool isHorizontallyMerged = cell.CellFormat.HorizontalMerge != CellMerge.None;
    bool isVerticallyMerged = cell.CellFormat.VerticalMerge != CellMerge.None;
    string cellLocation =
        $"R{cell.ParentRow.ParentTable.IndexOf(cell.ParentRow) + 1}, C{cell.ParentRow.IndexOf(cell) + 1}";

    if (isHorizontallyMerged && isVerticallyMerged)
        return $"The cell at {cellLocation} is both horizontally and vertically merged";
    if (isHorizontallyMerged)
        return $"The cell at {cellLocation} is horizontally merged.";

    return isVerticallyMerged ? $"The cell at {cellLocation} is vertically merged" : $"The cell at {cellLocation} is not merged";
}
```

يوضح كيفية دمج خلايا الجدول عموديًا.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل خلية في العمود الأول من الصف الأول.
// ستكون هذه الخلية هي الأولى في نطاق من الخلايا المدمجة رأسياً.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.First;
builder.Write("Text in merged cells.");

// أدخل خلية في العمود الثاني من الصف الأول، ثم قم بإنهاء الصف.
// أيضًا، قم بتكوين المنشئ لتعطيل الدمج الرأسي في الخلايا التي تم إنشاؤها.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.None;
builder.Write("Text in unmerged cell.");
builder.EndRow();

 // أدخل خلية في العمود الأول من الصف الثاني.
// بدلاً من إضافة محتويات نصية، سنقوم بدمج هذه الخلية مع الخلية الأولى التي أضفناها أعلاه مباشرة.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.Previous;

// أدخل خلية مستقلة أخرى في العمود الثاني من الصف الثاني.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.None;
builder.Write("Text in unmerged cell.");
builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "CellFormat.VerticalMerge.docx");
```

### أنظر أيضا

* enum [CellMerge](../../cellmerge/)
* class [CellFormat](../)
* مساحة الاسم [Aspose.Words.Tables](../../cellformat/)
* المجسم [Aspose.Words](../../../)


