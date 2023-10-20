---
title: Chart.SourceFullName
linktitle: SourceFullName
articleTitle: SourceFullName
second_title: Aspose.Words لـ .NET
description: Chart SourceFullName ملكية. يحصل على مسار واسم ملف xls/xlsx الذي يرتبط به هذا المخطط في C#.
type: docs
weight: 70
url: /ar/net/aspose.words.drawing.charts/chart/sourcefullname/
---
## Chart.SourceFullName property

يحصل على مسار واسم ملف xls/xlsx الذي يرتبط به هذا المخطط.

```csharp
public string SourceFullName { get; set; }
```

## أمثلة

يوضح كيفية الحصول على/تعيين الاسم الكامل لمستند xls/xlsx الخارجي إذا كان المخطط مرتبطًا.

```csharp
Document doc = new Document(MyDir + "Shape with linked chart.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

var sourceFullName = shape.Chart.SourceFullName;
Assert.True(sourceFullName.Contains("Examples\\Data\\Spreadsheet.xlsx"));

sourceFullName = "D:\\Documents\\ChartData.xlsx";
Assert.True(sourceFullName.Equals("D:\\Documents\\ChartData.xlsx", StringComparison.Ordinal));
```

### أنظر أيضا

* class [Chart](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
