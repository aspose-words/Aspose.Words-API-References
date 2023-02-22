---
title: Chart.SourceFullName
second_title: Aspose.Words لمراجع .NET API
description: Chart ملكية. يحصل على مسار واسم ملف xls / xlsx الذي يرتبط به هذا المخطط.
type: docs
weight: 60
url: /ar/net/aspose.words.drawing.charts/chart/sourcefullname/
---
## Chart.SourceFullName property

يحصل على مسار واسم ملف xls / xlsx الذي يرتبط به هذا المخطط.

```csharp
public string SourceFullName { get; set; }
```

### أمثلة

يوضح كيفية الحصول على الاسم الكامل لوثيقة xls / xlsx الخارجية إذا كان المخطط مرتبطًا.

```csharp
Document doc = new Document(MyDir + "Shape with linked chart.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.True(shape.Chart.SourceFullName.Contains("Examples\\Data\\Spreadsheet.xlsx"));
```

### أنظر أيضا

* class [Chart](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../chart/)
* المجسم [Aspose.Words](../../../)


