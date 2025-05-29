---
title: CellFormat.VerticalMerge
linktitle: VerticalMerge
articleTitle: VerticalMerge
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية CellFormat VerticalMerge لدمج الخلايا العمودية بسلاسة في جداول البيانات. حسّن تنظيم البيانات وعرضها بسهولة!
type: docs
weight: 130
url: /ar/net/aspose.words.tables/cellformat/verticalmerge/
---
## CellFormat.VerticalMerge property

يحدد كيفية دمج الخلية مع الخلايا الأخرى عموديًا.

```csharp
public CellMerge VerticalMerge { get; set; }
```

## ملاحظات

لا يمكن دمج الخلايا عموديا إلا إذا كانت حدودها اليمنى واليسرى متطابقة.

عندما يتم دمج الخلايا عموديًا، يتم دمج مناطق العرض للخلايا المدمجة. يتم استخدام المنطقة المدمجة لعرض محتويات الخلية الأولى المدمجة عموديًا ويجب أن تكون جميع الخلايا الأخرى المدمجة عموديًا فارغة.

## أمثلة

يطبع نوع الدمج الأفقي والرأسي للخلية.

```csharp
public void CheckCellsMerged()
{
    Document doc = new Document(MyDir + "Table with merged cells.docx");
    Table table = doc.FirstSection.Body.Tables[0];

    foreach (Row row in table.Rows)
        foreach (Cell cell in row.Cells)
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

يوضح كيفية دمج خلايا الجدول عموديا.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

//أدرج خلية في العمود الأول من الصف الأول.
// ستكون هذه الخلية هي الأولى في نطاق الخلايا المندمجة عموديًا.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.First;
builder.Write("Text in merged cells.");

//أدرج خلية في العمود الثاني من الصف الأول، ثم أنهِ الصف.
// قم أيضًا بتكوين المنشئ لتعطيل الدمج الرأسي في الخلايا التي تم إنشاؤها.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.None;
builder.Write("Text in unmerged cell.");
builder.EndRow();

 //أدرج خلية في العمود الأول من الصف الثاني.
//بدلاً من إضافة محتويات النص، سنقوم بدمج هذه الخلية مع الخلية الأولى التي أضفناها مباشرة أعلاه.
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
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
