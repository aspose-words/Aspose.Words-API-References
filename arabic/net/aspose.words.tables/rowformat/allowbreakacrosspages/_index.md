---
title: RowFormat.AllowBreakAcrossPages
second_title: Aspose.Words لمراجع .NET API
description: RowFormat ملكية. صواب في حالة السماح بتقسيم النص الموجود في صف الجدول عبر فاصل صفحة .
type: docs
weight: 10
url: /ar/net/aspose.words.tables/rowformat/allowbreakacrosspages/
---
## RowFormat.AllowBreakAcrossPages property

صواب في حالة السماح بتقسيم النص الموجود في صف الجدول عبر فاصل صفحة .

```csharp
public bool AllowBreakAcrossPages { get; set; }
```

### أمثلة

يوضح كيفية تعطيل تقسيم الصفوف عبر الصفحات لكل صف في الجدول.

```csharp
Document doc = new Document(MyDir + "Table spanning two pages.docx");
Table table = doc.FirstSection.Body.Tables[0];

// اضبط خاصية "AllowBreakAcrossPages" على "false" للاحتفاظ بالصف
// في قطعة واحدة إذا كان الجدول يمتد على صفحتين ، والتي تنقسم على طول هذا الصف.
// إذا كان الصف أكبر من أن يتسع في صفحة واحدة ، فسيقوم Microsoft Word بدفعه لأسفل إلى الصفحة التالية.
// اضبط خاصية "AllowBreakAcrossPages" على "true" للسماح للصف بالانفصال عبر صفحتين.
foreach (Row row in table.OfType<Row>())
    row.RowFormat.AllowBreakAcrossPages = allowBreakAcrossPages;

doc.Save(ArtifactsDir + "Table.AllowBreakAcrossPages.docx");
```

### أنظر أيضا

* class [RowFormat](../)
* مساحة الاسم [Aspose.Words.Tables](../../rowformat/)
* المجسم [Aspose.Words](../../../)


