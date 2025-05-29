---
title: CellMerge Enum
linktitle: CellMerge
articleTitle: CellMerge
second_title: Aspose.Words لـ .NET
description: اكتشف مجموعة Aspose.Words.Tables.CellMerge لدمج خلايا الجدول بكفاءة. حسّن تخطيطات مستنداتك بتكامل سلس ومرونته.
type: docs
weight: 7120
url: /ar/net/aspose.words.tables/cellmerge/
---
## CellMerge enumeration

يحدد كيفية دمج خلية في جدول مع خلايا أخرى.

```csharp
public enum CellMerge
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | لم يتم دمج الخلية. |
| First | `1` | الخلية هي الخلية الأولى في نطاق الخلايا المدمجة. |
| Previous | `2` | يتم دمج الخلية مع الخلية السابقة أفقيًا أو رأسيًا. |

## أمثلة

يوضح كيفية دمج خلايا الجدول أفقياً.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

//أدرج خلية في العمود الأول من الصف الأول.
// ستكون هذه الخلية هي الأولى في نطاق الخلايا المدمجة أفقيًا.
builder.InsertCell();
builder.CellFormat.HorizontalMerge = CellMerge.First;
builder.Write("Text in merged cells.");

// أدخل خلية في العمود الثاني من الصف الأول. بدلًا من إضافة محتوى نصي،
// سوف نقوم بدمج هذه الخلية مع الخلية الأولى التي أضفناها مباشرة إلى اليسار.
builder.InsertCell();
builder.CellFormat.HorizontalMerge = CellMerge.Previous;
builder.EndRow();

// أدخل خليتين غير مدمجتين إلى الصف الثاني.
builder.CellFormat.HorizontalMerge = CellMerge.None;
builder.InsertCell();
builder.Write("Text in unmerged cell.");
builder.InsertCell();
builder.Write("Text in unmerged cell.");
builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "CellFormat.HorizontalMerge.docx");
```

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

* مساحة الاسم [Aspose.Words.Tables](../../aspose.words.tables/)
* المجسم [Aspose.Words](../../)
