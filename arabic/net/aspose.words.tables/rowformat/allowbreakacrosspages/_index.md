---
title: RowFormat.AllowBreakAcrossPages
second_title: Aspose.Words لمراجع .NET API
description: RowFormat ملكية. صحيح إذا تم السماح للنص الموجود في صف الجدول بالانقسام عبر فاصل الصفحات.
type: docs
weight: 10
url: /ar/net/aspose.words.tables/rowformat/allowbreakacrosspages/
---
## RowFormat.AllowBreakAcrossPages property

صحيح إذا تم السماح للنص الموجود في صف الجدول بالانقسام عبر فاصل الصفحات.

```csharp
public bool AllowBreakAcrossPages { get; set; }
```

### أمثلة

يوضح كيفية تعطيل تقسيم الصفوف عبر الصفحات لكل صف في الجدول.

```csharp
Document doc = new Document(MyDir + "Table spanning two pages.docx");
Table table = doc.FirstSection.Body.Tables[0];

// اضبط الخاصية "AllowBreakAcrossPages" على "خطأ" للاحتفاظ بالصف
// قطعة واحدة إذا كان الجدول يمتد إلى صفحتين، مقسمتين على طول هذا الصف.
// إذا كان الصف كبيرًا جدًا بحيث لا يمكن احتواؤه في صفحة واحدة، فسيقوم Microsoft Word بدفعه إلى الصفحة التالية.
// قم بتعيين خاصية "AllowBreakAcrossPages" على "صحيح" للسماح للصف بالتقسيم عبر صفحتين.
foreach (Row row in table.OfType<Row>())
    row.RowFormat.AllowBreakAcrossPages = allowBreakAcrossPages;

doc.Save(ArtifactsDir + "Table.AllowBreakAcrossPages.docx");
```

### أنظر أيضا

* class [RowFormat](../)
* مساحة الاسم [Aspose.Words.Tables](../../rowformat/)
* المجسم [Aspose.Words](../../../)


