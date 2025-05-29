---
title: Chart.SourceFullName
linktitle: SourceFullName
articleTitle: SourceFullName
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Chart SourceFullName للوصول بسهولة إلى المسار واسم ملفات XLS/XLSX المرتبطة لتحسين تصور البيانات.
type: docs
weight: 100
url: /ar/net/aspose.words.drawing.charts/chart/sourcefullname/
---
## Chart.SourceFullName property

يحصل على المسار واسم ملف xls/xlsx الذي يرتبط به هذا الرسم البياني.

```csharp
public string SourceFullName { get; set; }
```

## أمثلة

يوضح كيفية الحصول على/تعيين الاسم الكامل للمستند الخارجي xls/xlsx إذا تم ربط الرسم البياني.

```csharp
Document doc = new Document(MyDir + "Shape with linked chart.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

var sourceFullName = shape.Chart.SourceFullName;
Assert.True(sourceFullName.Contains("Examples\\Data\\Spreadsheet.xlsx"));
```

### أنظر أيضا

* class [Chart](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
